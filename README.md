# Sublime-Preference
Personal Preference for Sublime - Majorly for Python Setup


Starting with level 0


1. Have Font Family Installed : Inconsolata  ( best one for programming)

2. Install Package Control - https://packagecontrol.io
3. Using Package Control, Install:

    -   Predawn Theme
    -   Flat Land Theme (as optional, but it looks good)
    -   Materialize Theme
    -   AutoPEP8  (#this is for python format checker)
    -   Anaconda    (# for autoPEP8 formating and linting, NOTE: Disable AutoPEP8 when using this.)
    -   SublimeREPL
    -   SublimeCodeIntel  (#for python autocompletion - IDE feature like)
    -   BracketHighlighter
    -   sidebar enhancements  (# for more option for file in sidebar)


#########################  Customize and Looks ##############################

4. Now Activate Predawn theme :

    -  Preferences > Setting > Preferences.Sublime-settings - User
        - delete every thing and paste this with braces:
                
                {
                "theme": "predawn-DEV.sublime-theme",
                "color_scheme": "Packages/Predawn/predawn.tmTheme", 
                }
            
    - save and exit sublime3.

5.  Choose a color Scheme from Materialize
        - preferences > color scheme > materialize > Brogramming
        - save and exit sublime3

6.  Add additional settings into "Preferences.Sublime-settings - User"

    - Paste these inside braces:
    
          "always_show_minimap_viewport": true,
          "font_face": "inconsolata",
          "font_size": 16,
          "gutter": true,
          "predawn_findreplace_small": true,
          "predawn_quick_panel_small": true,
          "predawn_sidebar_arrows": false,
          "predawn_sidebar_large": false,
          "predawn_sidebar_medium": false,
          "predawn_sidebar_narrow": false,
          "predawn_sidebar_small": false,
          "predawn_sidebar_xlarge": false,
          "predawn_sidebar_xsmall": true,
          "predawn_tabs_active_underline": false,
          "predawn_tabs_large": false,
          "predawn_tabs_medium": false,
          "predawn_tabs_small": true,
          "ignored_packages":
          [
              "Vintage"
          ],
          "line_padding_bottom": 1,
          "line_padding_top": 1,
          "match_brackets_content": false,
          "match_selection": false,
          "match_tags": true,
          "open_files_in_new_window": false,
          "overlay_scroll_bars": "enabled",
          "preview_on_click": true,
          "scroll_past_end": true,
          "scroll_speed": 5.0,
          "show_full_path": false,
          "sidebar_default": true,
          "translate_tabs_to_spaces": true,
          "trim_trailing_white_space_on_save": true,
          "word_wrap": true,
          "show_definitions": true,
          "show_encoding": true,
          "show_errors_inline": false,
          "save_on_focus_lost": false,
          "ensure_newline_at_eof_on_save": true,
          "highlight_modified_tabs": true,
          "use_simple_full_screen": true,
          "folder_exclude_patterns": [".svn", ".git", ".hg", "CVS"],
          "file_exclude_patterns": ["*.pyc", "*.pyo", "*.exe", "*.dll", "*.obj","*.o", "*.a", "*.lib", "*.so", "*.dylib", "*.ncb", "*.sdf", "*.suo", "*.pdb", "*.idb", ".DS_Store", "*.class", "*.psd", "*.sublime-workspace"],
          "font_options":
          [
              "subpixel_antialias"
          ],
          "bold_folder_labels": true,
          "caret_extra_width": 1,
          "caret_style": "phase",
          "close_windows_when_empty": false,
          "copy_with_empty_selection": false,
          "drag_text": false,
          "draw_minimap_border": true,
          "enable_tab_scrolling": false,
          "highlight_line": true,
          "highlight_modified_tabs": true,
          "shift_tab_unindent": true,
          "auto_complete_commit_on_tab": true
    

7. Anaconda Autoformater and linter Settings:

    Open up : Preferences -> package settings -> Anaconda -> Settings-User

    delete everything in there and Paste this:

        {       "anaconda_gutter_theme": "retina",
                "auto_formatting": true,
                "autoformat_ignore":
                [
                    "E309",
                    "E501"
                ],
                "pep8_ignore":
                [
                    "E309",
                    "E501"
                ],
                "anaconda_linter_underlines": true,

                "anaconda_linter_mark_style": "none",
                "display_signatures": false,
                "disable_anaconda_completion": false,
                "anaconda_tooltip_theme": "popup",
                "enable_signatures_tooltip": true,
                "enable_docstrings_tooltip": true,
        }



###################  Making Builds for running python programs  #################

8.  Make a new Build for running python programs  - Name it "myPython"     
    THIS is optional to make this build, coz if anaconda is installed, it gives its own build for python, Select that in Builds!
    But still if wanna, go ahead.

    -  Tools > Build System > New Build System
    -  Paste this with braces: (edit python.exe path, if changed during python install.)
    
        {

              "cmd": ["C:\\Users\\hp1\\AppData\\Local\\Programs\\Python\\Python36-32\\python.exe", "-u", "$file"],
              "file_regex": "^[]*file \"(...*?)\", line([0-9]*)",
              "selector": "source.python"

       }

9. Make another Build System - name it "REPL_python"

    - paste this in build file:

          {    
          "target": "run_existing_window_command",
          "id": "repl_python_run",
          "file": "config/Python/Main.sublime-menu"
          }

9. Now Ctrl + B, responds to running currently python program

10. Optional: switch between Theme, like change to Flatland theme by editing in preference > settings > Settings- User
    change in 'theme' value to Flatland Dark.sublime-theme

