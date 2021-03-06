ADD_DEFINITIONS(-DTESTDATA_DIR="${PROJECT_SOURCE_DIR}/testdata")

ADD_EXECUTABLE(sprites sprites.cc)
TARGET_LINK_LIBRARIES(sprites SDL2pp)

ADD_EXECUTABLE(lines lines.cc)
TARGET_LINK_LIBRARIES(lines SDL2pp)

ADD_EXECUTABLE(rendertarget rendertarget.cc)
TARGET_LINK_LIBRARIES(rendertarget SDL2pp)

ADD_EXECUTABLE(audio_sine audio_sine.cc)
TARGET_LINK_LIBRARIES(audio_sine SDL2pp)

ADD_EXECUTABLE(audio_wav audio_wav.cc)
TARGET_LINK_LIBRARIES(audio_wav SDL2pp)

IF(SDL2PP_WITH_IMAGE)
	ADD_EXECUTABLE(image image.cc)
	TARGET_LINK_LIBRARIES(image SDL2pp)

	ADD_EXECUTABLE(fill fill.cc)
	TARGET_LINK_LIBRARIES(fill SDL2pp)
ENDIF(SDL2PP_WITH_IMAGE)

IF(SDL2PP_WITH_TTF)
	ADD_EXECUTABLE(ttf ttf.cc)
	TARGET_LINK_LIBRARIES(ttf SDL2pp)
ENDIF(SDL2PP_WITH_TTF)

IF(SDL2PP_WITH_MIXER)
	ADD_EXECUTABLE(mixer mixer.cc)
	TARGET_LINK_LIBRARIES(mixer SDL2pp)

	ADD_EXECUTABLE(mixer_music mixer_music.cc)
	TARGET_LINK_LIBRARIES(mixer_music SDL2pp)

	ADD_EXECUTABLE(mixer_music_sine mixer_music_sine.cc)
	TARGET_LINK_LIBRARIES(mixer_music_sine SDL2pp)

	ADD_EXECUTABLE(mixer_effects mixer_effects.cc)
	TARGET_LINK_LIBRARIES(mixer_effects SDL2pp)
ENDIF(SDL2PP_WITH_MIXER)
