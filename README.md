# wordpress-magiclink
A Wordpress plugin that converts a selection on the editor to links directly

## Code

### Snippet to change content
```
function link_words( $text ) {
$replace = array(
'google' => '<a href="http://www.google.com">Google</a>',
'computer' => '<a href="http://www.myreferral.com">computer</a>',
'keyboard' => '<a href="http://www.myreferral.com/keyboard">buy keyboard here</a>'
);
$text = str_replace( array_keys($replace), $replace, $text );
return $text;
}
add_filter( 'the_content', 'link_words' );
add_filter( 'the_excerpt', 'link_words' );
```
