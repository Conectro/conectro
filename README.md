

<article class="markdown-body entry-content container-lg" itemprop="text">
  <h2>🌐 Conectro: The Ultimate Universal Terminal &amp; SSH Client</h2>

  <p><strong>Streamlined remote access, file management, and AI-powered workflows for power users and sysadmins.</strong></p>

  <p align="center">
    <img width="100%" alt="CVE-2026-41089 Abstract" src="https://github.com/Conectro/conectro/blob/main/banner.png" style="max-width: 100%; border-radius: 8px;">
  </p>

  <p>
<a href="https://conectro.org" rel="nofollow"><img src="https://img.shields.io/badge/Official%20Website%20%26%20Downloads-d90429?style=for-the-badge&amp;logo=web&amp;logoColor=white" alt="Official Website" style="max-width: 100%;"></a>
<a href="https://github.com/conectro/conectro" rel="nofollow"><img src="https://img.shields.io/badge/View%20Repository-00509d?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="View Source" style="max-width: 100%;"></a>
  </p>

  <hr>

  <h2>🧠 Conceptual Overview</h2>
  <p>
    I built <strong>Conectro</strong> because I was tired of juggling half a dozen different applications just to manage my infrastructure. I needed a single, unified workspace that functions as a Terminal, File Manager, and a multi-protocol client (SSH, SFTP, FTP, Telnet, SerialPort, RDP, VNC, and Spice). 
    <br><br>
    Whether you are managing legacy servers on outdated Linux distributions or orchestrating modern cloud deployments, this tool bridges the gap. I also integrated modern AI capabilities (OpenAI, DeepSeek) directly into the terminal to assist with command generation, script writing, and log analysis.
  </p>

  <h3>🎯 Core Philosophy</h3>
  <p>
    <em>"Connectivity should be limitless and frictionless."</em><br>
    Unlike native tools bound to a single ecosystem, I engineered Conectro to run everywhere. From bleeding-edge macOS and Windows environments down to legacy Windows 7, Ubuntu 18, and even specialized architectures like HarmonyOS, Android, and LoongArch (old-world &amp; new-world).
  </p>

  <hr>

  <h2>🚀 Quick Start &amp; Installation</h2>
  <p>I have made Conectro available across almost every major package manager. Choose the one that fits your workflow:</p>

  <h3>🍏 macOS</h3>
  <pre><code class="language-bash">brew install --cask conectro</code></pre>

  <h3>🪟 Windows (Winget &amp; Scoop)</h3>
  <pre><code class="language-powershell"># Using Winget
winget install conectro.conectro

# Using Scoop
scoop bucket add dorado https://github.com/chawyehsu/dorado
scoop install dorado/conectro</code></pre>

  <h3>🐧 Linux (Snap, APT &amp; NPM)</h3>
  <pre><code class="language-bash"># Snap Store
sudo snap install conectro --classic

# Global NPM installation
npm i -g conectro</code></pre>
  <p><em>Debian/RPM repositories and AppImages are also available on our <a href="https://conectro.org">homepage</a>.</em></p>

  <hr>

  <h2>📊 Protocol Architecture &amp; Integrations</h2>
  <pre><code class="language-mermaid">graph TD
    A[Conectro Core] --> B{Supported Protocols}
    B --> C[SSH / SFTP / FTP]
    B --> D[RDP / VNC / Spice]
    B --> E[Telnet / SerialPort]
    A --> F{AI &amp; Automation}
    F --> G[OpenAI / DeepSeek Integration]
    F --> H[MCP Widget / External Tools]
    A --> I[Cloud Sync]
    I --> J[GitHub Gist / WebDAV / Custom Server]</code></pre>

  <hr>

  <h2>🌐 OS Compatibility Matrix</h2>
  <p>I designed the application to be as inclusive as possible regarding operating systems and architectures:</p>
  <table>
    <thead>
      <tr>
        <th>OS / Platform</th>
        <th>Architecture</th>
        <th>Emoji</th>
        <th>Notes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Windows</strong></td>
        <td>x64 / ARM64</td>
        <td>🪟</td>
        <td>Supports Windows 7 and newer.</td>
      </tr>
      <tr>
        <td><strong>macOS</strong></td>
        <td>x64 / ARM64 (Apple Silicon)</td>
        <td>🍏</td>
        <td>Requires macOS 10.15 Catalina or higher.</td>
      </tr>
      <tr>
        <td><strong>Linux</strong></td>
        <td>x64 / ARM64 / Loong64</td>
        <td>🐧</td>
        <td>Supports older glibc (2.17+), Deepin, UOS, Kylin, Mint.</td>
      </tr>
      <tr>
        <td><strong>Mobile / Tablet</strong></td>
        <td>ARM</td>
        <td>📱</td>
        <td>Native Android and HarmonyOS builds available.</td>
      </tr>
      <tr>
        <td><strong>Web / Browser</strong></td>
        <td>Any</td>
        <td>🌐</td>
        <td>Check out <a href="https://github.com/conectro/conectro-web">conectro-web</a> for browser access.</td>
      </tr>
    </tbody>
  </table>

  <hr>

  <h2>✨ Key Features</h2>

  <h3>🤖 Built-in AI Assistant &amp; MCP Widget</h3>
  <p>
    I integrated an AI assistant that hooks into DeepSeek, OpenAI, or any compatible AI API (sponsored by Atlas Cloud, ApiMart, and ApiSmart). It can explain selected terminal output, suggest complex shell commands, and even generate UI themes. The newly added Model Context Protocol (MCP) widget allows seamless integration with external AI tools.
  </p>

  <h3>⚡ Advanced File Management &amp; Transfers</h3>
  <p>
    Beyond standard SFTP, I built in support for <strong>Zmodem (rz, sz)</strong> and <strong>Trzsz (trz/tsz)</strong>, which is fully compatible with tmux. You can even double-click remote files in the built-in file manager to edit them directly on the fly.
  </p>

  <h3>🔄 Global Sync &amp; Customization</h3>
  <p>
    Never lose your server lists. You can sync bookmarks, themes, and quick commands to GitHub/Gitee secret gists, standard WebDAV, a custom server, or the native Conectro Cloud. I also implemented a highly requested global hotkey feature (default <code>ctrl + 2</code>) to toggle window visibility instantly, similar to Guake.
  </p>

  <hr>

  <h2>🛠️ Advanced Use Cases</h2>

  <h3>🔗 Deep Link Support</h3>
  <p>You can launch sessions directly from your browser, scripts, or documentation using custom URI schemes:</p>
  <pre><code class="language-text">ssh://user@host:22
telnet://192.168.2.31:34554</code></pre>

  <h3>💻 Development &amp; Building from Source</h3>
  <p>If you want to contribute or build your own custom version (requires Node.js 24.x):</p>
  <pre><code class="language-bash">git clone git@github.com:conectro/conectro.git
cd conectro
npm config set legacy-peer-deps true
npm i

# Start Vite dev server
npm start

# In a separate terminal, launch the Electron app
npm run app</code></pre>

  <hr>

  <h2>⚖️ License &amp; Legal</h2>

  <h3>MIT License</h3>
  <pre><code>Copyright (c) Conectro Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...</code></pre>

  <h3>🚨 Disclaimer</h3>
  <blockquote>
    <p>
      <strong>This tool is provided for authorized system administration and development purposes.</strong>
      The maintainers assume no liability for misconfigurations, data loss during transfers, or unauthorized access resulting from leaked synchronization tokens or AI API keys. Always secure your credentials and utilize encrypted synchronization endpoints.
    </p>
  </blockquote>

  <hr>

  <h2>🔗 SEO Keywords (Naturally Integrated)</h2>
  <ul>
    <li>Cross-platform SSH client and terminal emulator</li>
    <li>SFTP file manager with Zmodem and Trzsz support</li>
    <li>RDP, VNC, and Spice remote desktop viewer</li>
    <li>AI-powered terminal command generator</li>
    <li>Windows, macOS, Linux, and HarmonyOS terminal tool</li>
    <li>Server management utility with cloud synchronization</li>
    <li>Deep linking SSH telnet URI handler</li>
  </ul>

  <hr>

  <h2>🔄 Download &amp; Community</h2>

  <p>
    <a href="https://conectro.org" rel="nofollow">
      <img
        src="https://img.shields.io/badge/Get%20Latest%20Release-d90429?style=for-the-badge&amp;logo=download&amp;logoColor=white"
        alt="Download"
        data-canonical-src="https://shields.io/badge/Get%20Latest%20Release-d90429?style=for-the-badge&amp;logo=download&amp;logoColor=white"
        style="max-width: 100%;">
    </a>
  </p>

  <p><strong>Ways to Support &amp; Contribute</strong>:</p>
  <ol>
    <li>Join our community discussions or submit an issue if you find a bug.</li>
    <li>Help translate the UI! We currently support 14+ languages, but improvements to <code>conectro-locales</code> are always welcome.</li>
    <li>Consider sponsoring the project via GitHub Sponsors, Ko-fi, or Crypto if this tool saves you hours of work every week!</li>
  </ol>

  <hr>

  <p><em>Conectro — The only remote connection manager you will ever need.</em></p>
</article>
