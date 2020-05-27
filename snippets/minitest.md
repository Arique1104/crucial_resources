##### Creates snippet that will setup a test file by running `setuptest`
<em><sub>nested within ```'.ruby.source':```</sub></em>

```coffeescript
'Test Setup':
  'prefix': 'setuptest'
  'body': """
  require_relative 'test_helper'

  class $1Test < Minitest::Test

    def setup
      $2
    end
  end
  """
```


OR

```ruby
'require "minitest"':
  'prefix': 'minitest'
  'body': 'require "minitest/autorun"\nrequire "minitest/pride"\nrequire "mocha/minitest"\n#require "./lib/<file_name>"\n\nclass ClassNameTest < Minitest::Test\n\n  #def setup\n\n  #end\n\n  #def test_it_exists\n    #assert_instance_of <Class>,\n  #end\n\n  #def test_it_has_attributes\n  #end\n\nend'
```
