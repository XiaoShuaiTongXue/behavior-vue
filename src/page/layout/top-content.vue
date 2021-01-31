<template>
  <div class="navbar-collapse collapse" style="-webkit-app-region: drag">
    <ul class="navbar-nav navbar-align">
      <li class="nav-item dropdown">
        <a class="nav-icon dropdown-toggle d-inline-block d-sm-none" href="#" data-toggle="dropdown">
          <i class="align-middle" data-feather="settings"></i>
        </a>

        <a class="nav-link dropdown-toggle d-none d-sm-inline-block" style="-webkit-app-region: no-drag" data-toggle="dropdown">
          <img src="images/avatar.jpg" class="avatar img-fluid rounded mr-1" alt="Charles Hall"/>
          <span class="text-dark">小明</span>
        </a>
        <div class="dropdown-menu dropdown-menu-right">
          <a class="dropdown-item" ><i class="align-middle mr-1"
                                       data-feather="user"></i> 个人资料修改</a>
          <a class="dropdown-item" ><i class="align-middle mr-1"
                                       data-feather="help-circle"></i> 帮助中心</a>
          <div class="dropdown-divider"></div>
          <a class="dropdown-item" id="exit_a">登出</a>
        </div>
      </li>
    </ul>
  </div>
</template>
<script></script>
<style></style>
