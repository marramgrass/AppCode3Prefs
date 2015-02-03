require 'rake'

desc "Carrying around my preferences for AppCode 3.x"
task :install do

  Dir.glob('*') do |folder_name|
  	if File.directory?(folder_name)
  	  target_folder = "#{ENV['HOME']}/Library/Preferences/appCode31/"
  	  target_folder_name = "#{target_folder}#{folder_name}"

  	  if File.exists?(target_folder_name)
  	  	`mv "#{target_folder_name}" "#{target_folder_name}.backup"`
  	  end

  	  `ln -s "$PWD/#{folder_name}/" "#{target_folder_name}"`
  	end
  end

end

task :uninstall do

  target_folder = "#{ENV['HOME']}/Library/Preferences/appCode31/"
  Dir.glob(target_folder + '*.backup') do |backup_folder_name|
  	link_name = backup_folder_name.chomp('.backup')

  	if File.directory?(backup_folder_name) && File.exists?(link_name)
  	  `rm #{link_name}`
  	  `mv #{backup_folder_name} #{link_name}`
  	end
  end

end
