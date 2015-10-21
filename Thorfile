require 'thor/group'

module Middleman
  class Generator < ::Thor::Group
    include ::Thor::Actions

    source_root File.expand_path(File.dirname(__FILE__))

    def copy_default_files
      directory 'template', '.', exclude_pattern: /\.DS_Store$/
    end

    def build_gemfile
      insert_into_file 'Gemfile', "gem 'middleman-livereload'\n", after: "# Middleman Gems\n"
      insert_into_file 'Gemfile', "gem 'middleman-sprockets', '>= 4.0.0.rc.1'\n", after: "# Middleman Gems\n"
      insert_into_file 'Gemfile', "gem 'middleman', '>= 4.0.0.rc.1'\n", after: "# Middleman Gems\n"
    end
  end
end

