<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 2:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:29:59</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:30:00</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:30:00</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:30:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:30:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-09-02&nbsp;18:30:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-09-02&nbsp;18:28:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-09-02&nbsp;18:28:18</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-09-02&nbsp;18:28:18</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Win</a></td><td align="left">2023-09-02&nbsp;18:28:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-09-02&nbsp;18:25:46</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-09-02&nbsp;18:25:47</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-09-02&nbsp;18:25:48</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Espressobin</a></td><td align="left">2023-09-02&nbsp;18:25:49</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-09-02&nbsp;18:28:56</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-09-02&nbsp;18:28:57</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-09-02&nbsp;18:28:57</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Pine H64</a></td><td align="left">2023-09-02&nbsp;18:28:58</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-09-02&nbsp;18:29:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-09-02&nbsp;18:29:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-09-02&nbsp;18:29:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">RockPro 64</a></td><td align="left">2023-09-02&nbsp;18:29:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-09-02&nbsp;18:29:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-09-02&nbsp;18:29:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-09-02&nbsp;18:29:18</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi E</a></td><td align="left">2023-09-02&nbsp;18:29:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-09-02&nbsp;18:27:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-09-02&nbsp;18:27:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-09-02&nbsp;18:27:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C2</a></td><td align="left">2023-09-02&nbsp;18:27:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/quvufujuwa">NanoPi R6S</a></td><td align="left">2023-09-02&nbsp;18:31:10</td><td align=right>5.10.160-legacy-rk35xx</td><td align=right>2410</td><td align=right>15838</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-09-02&nbsp;18:27:14</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-09-02&nbsp;18:27:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-09-02&nbsp;18:27:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid C4</a></td><td align="left">2023-09-02&nbsp;18:27:16</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-09-02&nbsp;18:29:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-09-02&nbsp;18:29:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-09-02&nbsp;18:29:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi 4B</a></td><td align="left">2023-09-02&nbsp;18:29:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-09-02&nbsp;18:26:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-09-02&nbsp;18:26:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-09-02&nbsp;18:26:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi M4</a></td><td align="left">2023-09-02&nbsp;18:26:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi S</a></td><td align="left">2023-09-02&nbsp;18:47:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi S</a></td><td align="left">2023-09-02&nbsp;18:47:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi S</a></td><td align="left">2023-09-02&nbsp;18:47:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rockpi S</a></td><td align="left">2023-09-02&nbsp;18:47:11</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-09-02&nbsp;18:25:25</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-09-02&nbsp;18:25:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-09-02&nbsp;18:25:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi Pro</a></td><td align="left">2023-09-02&nbsp;18:25:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid XU4</a></td><td align="left">2023-09-02&nbsp;18:27:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid XU4</a></td><td align="left">2023-09-02&nbsp;18:27:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid XU4</a></td><td align="left">2023-09-02&nbsp;18:27:35</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid XU4</a></td><td align="left">2023-09-02&nbsp;18:27:35</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:16</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:18</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ZeroPi</a></td><td align="left">2023-09-02&nbsp;18:30:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-09-02&nbsp;18:25:20</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-09-02&nbsp;18:25:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-09-02&nbsp;18:25:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-09-02&nbsp;18:25:24</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-09-02&nbsp;18:26:53</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-09-02&nbsp;18:26:54</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-09-02&nbsp;18:26:55</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R4S</a></td><td align="left">2023-09-02&nbsp;18:26:56</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-09-02&nbsp;18:27:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-09-02&nbsp;18:27:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-09-02&nbsp;18:27:23</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Odroid N2</a></td><td align="left">2023-09-02&nbsp;18:27:24</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-09-02&nbsp;18:26:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-09-02&nbsp;18:26:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-09-02&nbsp;18:26:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 3</a></td><td align="left">2023-09-02&nbsp;18:26:46</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-09-02&nbsp;18:28:40</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-09-02&nbsp;18:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-09-02&nbsp;18:28:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus</a></td><td align="left">2023-09-02&nbsp;18:28:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-09-02&nbsp;18:28:27</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-09-02&nbsp;18:28:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-09-02&nbsp;18:28:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero2</a></td><td align="left">2023-09-02&nbsp;18:28:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-09-02&nbsp;18:25:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-09-02&nbsp;18:25:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-09-02&nbsp;18:25:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Clearfog Pro</a></td><td align="left">2023-09-02&nbsp;18:25:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ODROID M1</a></td><td align="left">2023-09-02&nbsp;18:27:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">ODROID M1</a></td><td align="left">2023-09-02&nbsp;18:27:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-09-02&nbsp;18:29:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-09-02&nbsp;18:29:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-09-02&nbsp;18:29:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board 2</a></td><td align="left">2023-09-02&nbsp;18:29:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-09-02&nbsp;18:27:38</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-09-02&nbsp;18:27:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-09-02&nbsp;18:27:40</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi 4 LTS</a></td><td align="left">2023-09-02&nbsp;18:27:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-09-02&nbsp;18:26:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-09-02&nbsp;18:26:13</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-09-02&nbsp;18:26:13</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Le potato</a></td><td align="left">2023-09-02&nbsp;18:26:14</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-09-02&nbsp;18:25:15</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-09-02&nbsp;18:25:17</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-09-02&nbsp;18:25:18</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-09-02&nbsp;18:25:19</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-09-02&nbsp;18:25:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-09-02&nbsp;18:25:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-09-02&nbsp;18:25:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi M5</a></td><td align="left">2023-09-02&nbsp;18:25:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-09-02&nbsp;18:29:35</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-09-02&nbsp;18:29:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-09-02&nbsp;18:29:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-09-02&nbsp;18:29:38</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-09-02&nbsp;18:25:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-09-02&nbsp;18:25:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Udoo</a></td><td align="left">2023-09-02&nbsp;18:29:43</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Udoo</a></td><td align="left">2023-09-02&nbsp;18:29:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Udoo</a></td><td align="left">2023-09-02&nbsp;18:29:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Udoo</a></td><td align="left">2023-09-02&nbsp;18:29:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-09-02&nbsp;18:25:53</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-09-02&nbsp;18:25:54</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-09-02&nbsp;18:25:55</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM2</a></td><td align="left">2023-09-02&nbsp;18:25:57</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM3</a></td><td align="left">2023-09-02&nbsp;18:25:59</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM3</a></td><td align="left">2023-09-02&nbsp;18:26:00</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM3</a></td><td align="left">2023-09-02&nbsp;18:26:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM3</a></td><td align="left">2023-09-02&nbsp;18:26:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:38</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi Neo 2 Black</a></td><td align="left">2023-09-02&nbsp;18:26:40</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-09-02&nbsp;18:26:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-09-02&nbsp;18:26:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-09-02&nbsp;18:26:04</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Khadas VIM1</a></td><td align="left">2023-09-02&nbsp;18:26:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:38</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-09-02&nbsp;18:28:40</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-09-02&nbsp;18:27:59</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-09-02&nbsp;18:28:00</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-09-02&nbsp;18:28:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1</a></td><td align="left">2023-09-02&nbsp;18:28:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Nanopi R2S</a></td><td align="left">2023-09-02&nbsp;18:26:42</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Nanopi R2S</a></td><td align="left">2023-09-02&nbsp;18:26:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Nanopi R2S</a></td><td align="left">2023-09-02&nbsp;18:26:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Nanopi R2S</a></td><td align="left">2023-09-02&nbsp;18:26:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">NanoPi R1</a></td><td align="left">2023-09-02&nbsp;18:26:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:27:59</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:28:00</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:28:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:28:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:28:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi One+</a></td><td align="left">2023-09-02&nbsp;18:28:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-09-02&nbsp;18:29:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-09-02&nbsp;18:29:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-09-02&nbsp;18:28:01</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-09-02&nbsp;18:28:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-09-02&nbsp;18:28:02</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-09-02&nbsp;18:28:03</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-09-02&nbsp;18:28:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-09-02&nbsp;18:28:39</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-09-02&nbsp;18:28:40</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-09-02&nbsp;18:28:41</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
