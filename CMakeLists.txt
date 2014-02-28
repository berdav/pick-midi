#Cmake file for pick-midi project

project(PickMidi)
cmake_minimum_required(VERSION 2.8)

set(PICKMIDI_VERSION_MAJOR 0)
set(PICKMIDI_VERSION_MINOR 0)
set(PICKMIDI_VERSION_SUBMINOR 1)


add_executable(PickMidi pick-midi/src/pickmidi.c pick-midi/src/fft.c pick-midi/src/fft_note_finder.c)
#link_directories(/usr/lib)
target_link_libraries(PickMidi fftw3 m)
