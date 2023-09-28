
set(RTSP_SERVER_LIST 
	rtsp-server/rtsp-address-pool.c
	rtsp-server/rtsp-auth.c
	rtsp-server/rtsp-client.c
	rtsp-server/rtsp-context.c
	rtsp-server/rtsp-media-factory-uri.c
	rtsp-server/rtsp-media-factory.c
	rtsp-server/rtsp-media.c
	rtsp-server/rtsp-mount-points.c
	rtsp-server/rtsp-params.c
	rtsp-server/rtsp-permissions.c
	rtsp-server/rtsp-sdp.c
	rtsp-server/rtsp-server.c
	rtsp-server/rtsp-session-media.c
	rtsp-server/rtsp-session-pool.c
	rtsp-server/rtsp-session.c
	rtsp-server/rtsp-stream-transport.c
	rtsp-server/rtsp-stream.c
	rtsp-server/rtsp-thread-pool.c
	rtsp-server/rtsp-token.c
)

set(RTSP_SINK_LIST 
	rtsp-sink/gstrtspclientsink.c
	rtsp-sink/plugin.c
)


add_library(gstrtspserver SHARED 
	${RTSP_SERVER_LIST} 
	${RTSP_SINK_LIST}
)
