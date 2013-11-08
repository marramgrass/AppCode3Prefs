require 'rake'

desc "Carrying around my preferences for AppCode 2.x"
task :install do

  Dir.glob('*') do |folder_name|
  	if File.directory?(folder_name)
  	  target_folder = "#{ENV['HOME']}/Library/Preferences/appCode20/"
  	  target_folder_name = "#{target_folder}#{folder_name}"

  	  if File.exists?(target_folder_name)
  	  	`mv "#{target_folder_name}" "#{target_folder_name}.backup"`
  	  end

  	  `ln -s "$PWD/#{folder_name}/" "#{target_folder_name}"`
  	end
  end

end
