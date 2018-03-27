/* This allows you to insert content into a page limiting it's visibility to only certain roles.
Inside the content on any wordpress page wrap what you want to hide inside this shortcode.

Example....

Welcome to the site, you can view this
[editor_or_higher] Secret Stuff Here [/editor_or_higher]
and this too.

*/

function editor_or_higher_fx( $atts, $content = null ) {
	$user = wp_get_current_user();
	$allowed_roles = array('editor', 'administrator'); //names of the roles you want to be able to view this content
	if( array_intersect($allowed_roles, $user->roles ) ) {
		return '<span class="caption">' . do_shortcode($content) . '</span>';
	}

}
add_shortcode( 'editor_or_higher', 'editor_or_higher_fx' );
