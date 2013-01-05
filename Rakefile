desc "installs vimfiles"
task :default => [:setup_symlinks, :bundle_install]

desc "Create Symlinks"
task :setup_symlinks do
  Dir.glob('**/*.symlink', File::FNM_DOTMATCH).each do |linkable|
    target = File.expand_path(File.join("~", linkable.gsub(".symlink", "")))

    # Skip if this file already exists as a symlink to the current file
    next if File.exists?(target) && File.ftype(target) == 'link' \
            && File.identical?(linkable, target)

    if File.exist?(target) || File.symlink?(target)
      puts "File already exists: #{target}, overwrite? [y]es, [n]o"
      response = STDIN.gets.chomp.downcase
      next if response == "n"
      if response == "y"
        puts "Overwriting #{target}"
        FileUtils.rm_rf target
      end
    end

    File.symlink File.expand_path(linkable), target
  end
end

desc "Update vim bundles"
task :bundle_install do
  sh "vim -c :BundleInstall -c :q -c :q"
end
