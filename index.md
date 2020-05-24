---
title: Terminal++
layout: default
---

<h1 class="display-3"><img alt="logo" src="favicon.png" /> Terminal++</h1>
<p class="lead">
    <code>terminalpp</code> is a minimalist but powerful terminal emulator which provides almost identical features and user experience on all major operating systems - Windows, Linux and macOS. 
</p>

<div class="row justify-content-center">
    <!-- Windows downloads -->
    <div class="btn-group btn-download">
      <button role="button" class="btn btn-dark btn-lg" onclick="window.location='https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.msi'">
          <i class="fab fa-windows"></i> Windows
      </button>
    </div>
    <!-- Linux downloads -->
    <div class="btn-group btn-download">
      <button type="button" class="btn btn-dark btn-lg" onclick="window.location='https://snapcraft.io/terminalpp'">
          <i class="fab fa-linux"></i> Linux
      </button>
      <button type="button" class="btn btn-dark dropdown-toggle dropdown-toggle-split" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        <span class="sr-only">Toggle Dropdown</span>
      </button>
      <div class="dropdown-menu">
        <a class="dropdown-item" href="https://snapcraft.io/terminalpp">snap
            <i class="fab fa-linux"></i>
        </a>
        <a class="dropdown-item" href="https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.deb">deb
            <i class="fab fa-ubuntu"></i>
        </a>
        <a class="dropdown-item" href="https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.rpm">rpm
            <i class="fab fa-suse"></i>
            <i class="fab fa-redhat"></i>
            <i class="fab fa-fedora"></i>
        </a>
      </div>
    </div>
    <!-- macOS downloads -->
    <div class="btn-group btn-download">
      <button type="button" class="btn btn-dark btn-lg" onclick="window.location='https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp-macos.zip'">
          <i class="fab fa-apple"></i> macOS
      </button>
    </div>
</div>

<div id="carouselExampleFade" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="resources/screenshots/windows.png" class="d-block" alt="...">
    </div>
    <div class="carousel-item">
      <img src="resources/screenshots/linux.png" class="d-block" alt="...">
    </div>
    <div class="carousel-item">
      <img src="resources/screenshots/macos.png" class="d-block" alt="...">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleFade" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleFade" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

<!-- TODO generate this perhaps -->

<h1 class="display-4 text-center h-divider">Feature Highlights</h1>

<div class="row row-cols-1 row-cols-md-3">

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title">Cross-platform</h5>
        <p class="card-text">
            <code>terminalpp</code> natively supports Windows 10 and Linux and works on macOS via a Qt renderer.
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title"><a href="/features/pty-bypass.html">Fast</a></h5>
        <p class="card-text">
            On native platforms <code>terminalpp</code> is either on par, or faster than really fast emulators such as alacritty. Order(s) of magnitude faster on Windows with ConPTY bypass.
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title"><a href="/features/configuration.html">Fonts &amp; Colors</a></h5>
        <p class="card-text">
            Support for all possible colors (16M) and native font fallback for extra characters. CJK, double width and double size characters support..
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title"><a href="/features/clipboard.html">Clipboard</a></h5>
        <p class="card-text">
            Bi-directional clipboard. Primary and clipboard buffers on Linux, clipboard and emulated primary buffer in Windows. Paste preview is supported.
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title">Zoom</h5>
        <p class="card-text">
            <code>ctrl-</code> and <code>ctrl=</code> to fast zoom in & out similar to web browsers and other GUI apps.        
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title">History</h5>
        <p class="card-text">
            Remembers terminal output outside of the visible area when it matters.
        </p>
      </div>
    </div>  
  </div>

  <div class="col mb-4">
    <div class="card h-100">
      <!-- <img src="..." class="card-img-top" alt="..."> -->
      <div class="card-body">
        <h5 class="card-title"><a href="/features/remote-files.html">Remote Files</a></h5>
        <p class="card-text">
            Allows opening files from remote servers the terminal is connected to on local computer via the <code>ropen</code> command. Supports <code>tmux</code> passthrough.
        </p>
      </div>
    </div>  
  </div>

</div>