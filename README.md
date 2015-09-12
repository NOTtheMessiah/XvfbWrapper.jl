# XvfbWrapper.jl

As the name implies, this is a Julia wrapper for X virtual framebuffer. You can run graphical programs on it without outputting to a physical screen. As of this point in development, it is intended for use with automated testing on servers which may not have a physical display (note, you still need the Xserver packages).

This code was originally ported from Python's xfvbwrapper [(source)](https://github.com/cgoldberg/xvfbwrapper) [(PyPI)](http://pypi.python.org/pypi/xvfbwrapper) by Corey Goldberg 

# Install

	julia> Pkg.clone("https://github.com/NOTtheMessiah/XvfbWrapper.jl.git")

#### Prerequisites

	sudo apt-get install xvfb

	sudo pacman -S xorg-server-xvfb

# Usage

	using XvfbWrapper
	fb = Xvfb()
	start!(fb)

	run(`$(your_program_here)`)

	stop!(fb)
 
