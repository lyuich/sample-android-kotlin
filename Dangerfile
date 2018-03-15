# github comment settings
github.dismiss_out_of_range_messages

# for PR
if github.pr_title.include?('[WIP]') || github.pr_labels.include?('WIP')
  warn('PR is classed as Work in Progress')
end

# Warn when there is a big PR
warn('a large PR') if git.lines_of_code > 300

# ktlint
checkstyle_format.base_path = Dir.pwd
checkstyle_format.report 'app/build/reports/ktlint/ktlint-debug.xml'

# AndroidLint
android_lint.report_file = "app/build/reports/lint-results.xml"
android_lint.skip_gradle_task = true
android_lint.severity = "Error"
android_lint.lint(inline_mode: true)
