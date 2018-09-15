# weechat.randy
My Personal WeeChat config
Forked from fats/weechat_theme.txt

/script install iset.pl
/script install buffers.pl
/script install colorize_nicks.py

/set weechat.look.buffer_notify_default message
/set weechat.look.color_nick_offline on
/set weechat.look.prefix_action " •"
/set weechat.look.prefix_join "»"
/set weechat.look.prefix_network "▬▬"
/set weechat.look.prefix_quit "«"
/set weechat.look.prefix_same_nick "⤷"
/set weechat.look.prefix_suffix "│"
/set weechat.look.read_marker_string "─"
/set weechat.look.separator_horizontal ""
/set weechat.look.scroll_page_percent 50

/set weechat.color.chat_channel darkgray
/set weechat.color.chat_delimiters darkgray
/set weechat.color.chat_highlight_bg 60
/set weechat.color.chat_host darkgray
/set weechat.color.chat_nick darkgray
/set weechat.color.chat_nick_colors "cyan,magenta,green,brown,lightblue,default,lightcyan,lightmagenta,lightgreen,blue,31,35,38,40,49,63,70,80,92,99,112,126,130,138,142,148,160,162,167,169,174,176,178,184,186,210,212,215,247"

/set weechat.color.chat_nick_offline darkgray
/set weechat.color.chat_prefix_action darkgray
/set weechat.color.chat_prefix_join 24
/set weechat.color.chat_prefix_network darkgray
/set weechat.color.chat_prefix_quit 23
/set weechat.color.chat_prefix_suffix 16
/set weechat.color.chat_read_marker 16
/set weechat.color.chat_tags darkgray
/set weechat.color.chat_time darkgray
/set weechat.color.chat_time_delimiters 234
/set weechat.color.nicklist_away 244
/set weechat.color.separator 16

/set weechat.bar.buffers.hidden off
/set weechat.bar.buffers.items "buffers"
/set weechat.bar.isetbar.items "isetbar_help"
/set weechat.bar.status.color_bg 234
/set weechat.bar.title.color_bg 234

/set irc.look.color_nicks_in_names on
/set irc.look.color_nicks_in_server_messages off

/set irc.color.message_join darkgray
/set irc.color.message_quit darkgray
/set irc.color.reason_quit darkgray

/set iset.color.bg_selected 234
/set iset.help.show_plugin_description on

/set colorize_nicks.look.colorize_input on
/set colorize_nicks.look.ignore_tags "irc_join,irc_part,irc_quit"

/set script.color.text_bg_selected 234

/set buffers.color.current_bg 60
/set buffers.color.current_fg white
/set buffers.color.number 31
/set buffers.color.number_char 31

/set buffers.look.hide_merged_buffers all
/set buffers.look.hotlist_counter on
/set buffers.look.mark_inactive on
/set buffers.look.number_char " "

/trigger add url modifier weechat_print "${tg_tags} !~ irc_quit" ";[a-z]+://\S+;${color:228}${color:underline}${re:0}${color:reset};" ""
/trigger add nick modifier weechat_print "${tg_tags} =~ irc_nick" ";is now known as;${color:darkgray}is now known as;" ""
/trigger add disconnect modifier "weechat_print" "${tg_tags} !~ . && ${tg_buffer} !~ irc.server." ";irc: disconnected from server;${color:red}irc: disconnected from server;" ""

/key bind meta-, /window scroll_up
/key bind meta-- /window scroll_down
