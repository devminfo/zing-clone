<script setup lang="ts">
const isExpanded = ref(true)
const activeMenu = ref('1')

const handleSelect = (key: string) => {
  // console.log(key)
}
</script>

<template>
  <div class="fixed h-screen">
    <div
      class="sidebar-wrap flex flex-col flex-start"
      :class="{ 'is-expanded': isExpanded }"
    >
      <!-- logo -->
      <div class="sidebar-logo h-[70px]">
        <span class="logo"></span>
      </div>

      <!-- menu -->
      <el-menu
        class="sidebar-menu flex flex-col flex-1 overflow-hidden"
        :default-active="activeMenu"
        @select="handleSelect"
      >
        <!-- menu top -->
        <div class="menu-main">
          <el-menu-item index="1" class="menu-item">
            <el-icon :size="24" class="menu-icon">
              <Icon name="material-symbols:explore-outline" opacity="0.8" />
            </el-icon>

            <span class="menu-title">Khám Phá</span>
          </el-menu-item>

          <el-menu-item index="2" class="menu-item">
            <el-icon :size="24" class="menu-icon">
              <Icon name="ic:baseline-auto-graph" opacity="0.8" />
            </el-icon>

            <span class="menu-title">#zingchart</span>

            <el-icon :size="20" class="play-button">
              <Icon name="bx:play-circle" />
            </el-icon>
          </el-menu-item>

          <el-menu-item index="3" class="menu-item">
            <el-icon :size="24" class="menu-icon">
              <Icon name="mdi:music-circle-outline" opacity="0.8" />
            </el-icon>

            <span class="menu-title flex"
              >Radio

              <img
                class="ml-1 md:inline hidden pb-0.5"
                src="https://zjs.zmdcdn.me/zmp3-desktop/dev/147506/static/media/live-tag.e25dd240.svg"
                alt=""
              />
            </span>

            <el-icon :size="20" class="play-button">
              <Icon name="bx:play-circle" />
            </el-icon>
          </el-menu-item>

          <el-menu-item index="4" class="menu-item">
            <el-icon :size="24" class="menu-icon">
              <Icon name="bx:library" opacity="0.8" />
            </el-icon>

            <span class="menu-title">Thư Viện</span>

            <el-icon :size="20" class="play-button">
              <Icon name="bx:play-circle" />
            </el-icon>
          </el-menu-item>
        </div>

        <!-- divider -->
        <el-divider class="sidebar-divider" />

        <!-- menu center -->
        <div class="scroll-box flex-1 overflow-y-auto">
          <el-menu-item index="5" class="menu-item">
            <el-icon :size="22" class="menu-icon">
              <Icon name="solar:music-notes-linear" opacity="0.8" />
            </el-icon>

            <span class="menu-title">BXH nhạc mới</span>

            <el-icon :size="20" class="play-button">
              <Icon name="bx:play-circle" />
            </el-icon>
          </el-menu-item>

          <el-menu-item index="6" class="menu-item">
            <el-icon :size="22" class="menu-icon">
              <Icon name="iconoir:grid-add" opacity="0.8" />
            </el-icon>

            <span class="menu-title">Chủ Đề & Thể Loại</span>
          </el-menu-item>

          <el-menu-item index="7" class="menu-item">
            <el-icon :size="22" class="menu-icon">
              <Icon name="iconoir:star" opacity="0.8" />
            </el-icon>

            <span class="menu-title">Top 100</span>
          </el-menu-item>

          <div class="vip-banner-sidebar hidden md:block">
            <div class="text">
              Nghe nhạc không quảng cáo cùng kho nhạc PREMIUM
            </div>
            <a
              class="zm-btn is-medium is-outlined is-upper button"
              tabindex="0"
              href="https://zingmp3.vn/vip?utm_source=desktop&amp;utm_campaign=VIP&amp;utm_medium=sidebar"
              target="_blank"
              >Nâng cấp tài khoản</a
            >
          </div>

          <div class="mt-6">
            <el-menu-item
              index="4"
              class="menu-item bg-transparent! border-transparent!"
            >
              <el-icon
                :size="24"
                class="menu-icon bg-[#8843ff] rounded-full p-0.5"
              >
                <Icon name="bx:history" />
              </el-icon>

              <span class="menu-title">Nghe gần đây</span>

              <el-icon :size="20" class="play-button">
                <Icon name="bx:play-circle" />
              </el-icon>
            </el-menu-item>

            <el-menu-item
              index="4"
              class="menu-item bg-transparent! border-transparent!"
            >
              <el-icon
                :size="24"
                class="menu-icon bg-[#14c7ff] rounded-full p-0.5"
              >
                <Icon name="humbleicons:heart" />
              </el-icon>

              <span class="menu-title">Bài hát yêu thích</span>
            </el-menu-item>

            <el-menu-item
              index="4"
              class="menu-item bg-transparent! border-transparent!"
            >
              <el-icon
                :size="24"
                class="menu-icon bg-[#fa7130] rounded-full p-0.5"
              >
                <Icon name="solar:playlist-minimalistic-2-outline" />
              </el-icon>

              <span class="menu-title">Playlist</span>
            </el-menu-item>

            <el-menu-item
              index="4"
              class="menu-item bg-transparent! border-transparent!"
            >
              <el-icon
                :size="24"
                class="menu-icon bg-[#ff4daf] rounded-full p-0.5"
              >
                <Icon name="iconamoon:music-album-light" />
              </el-icon>

              <span class="menu-title">Album</span>
            </el-menu-item>

            <el-menu-item
              index="4"
              class="menu-item bg-transparent! border-transparent!"
            >
              <el-icon
                :size="24"
                class="menu-icon bg-[#ff4e4e] rounded-full p-0.5"
              >
                <Icon name="bx:cloud-upload" />
              </el-icon>

              <span class="menu-title">Đã tải lên</span>
            </el-menu-item>
          </div>

          <!-- divider -->
          <el-divider class="sidebar-divider" />
        </div>
      </el-menu>

      <div class="footer">
        <el-radio-group v-model="isExpanded" style="margin-bottom: 20px">
          <el-radio-button :label="true">expand</el-radio-button>
          <el-radio-button :label="false">collapse</el-radio-button>
        </el-radio-group>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.sidebar-wrap {
  @apply w-[70px] h-full bg-[var(--sidebar-popup-bg)] md:w-[240px] md:bg-[var(--sidebar-bg)];
}

.sidebar-logo {
  @apply w-full flex justify-center items-center pb-[6px] md:pb-0 md:pl-7 md:justify-start;
}

.logo {
  @apply w-[45px] h-[45px] bg-contain bg-no-repeat md:w-[120px] md:h-[40px];

  background-image: var(--logo-icon-url);

  @screen md {
    background-image: var(--logo-url);
  }
}

.sidebar-menu {
  @apply border-r-0 bg-transparent;
}

.menu-item {
  @apply flex items-center leading-5 font-medium px-3 py-5 h-[48px];
  color: var(--navigation-text);
  border-left: 3px solid transparent;

  &:hover {
    @apply bg-transparent;
    color: var(--text-item-hover);
  }

  &.is-active {
    @apply bg-[var(--alpha-bg)] md:border-l-[var(--purple-primary)];
    color: var(--text-item-hover);
  }

  .menu-icon {
    @apply mr-3;
  }

  .menu-title {
    @apply hidden md:inline md:flex-1;
  }

  .play-button {
    @apply hidden md:display-inherit md:invisible md:opacity-0 md:transition-all;
  }

  &:hover .play-button {
    @apply md:visible md:opacity-100;
  }
}

.el-divider {
  @apply my-4 w-[24px] md:w-[80%] mx-auto border-[var(--border-primary)];
}

.is-expanded {
  @apply w-[240px];

  .sidebar-logo {
    @apply pb-0 pl-7 justify-start;
  }

  .logo {
    @apply w-[120px] h-[40px];
    background-image: var(--logo-url);
  }

  .el-menu .el-menu-item {
    &.is-active {
      @apply border-[var(--purple-primary)];
    }

    .menu-title {
      @apply inline;
    }
  }

  .el-divider {
    @apply w-[80%];
  }
}

.vip-banner-sidebar {
  padding: 15px 8px;
  border-radius: 8px;
  margin: 20px 20px;
  text-align: center;
  background-image: linear-gradient(117deg, #5a4be7, #c86dd7 102%);
}

.vip-banner-sidebar .text {
  font-size: 12px;
  margin-bottom: 10px;
  font-weight: 600;
  border-color: #ffdb00;
  line-height: 1.67;
  color: var(--white);
}

.vip-banner-sidebar .zm-btn {
  background-color: #ffdb00;
  border-color: #ffdb00;
  color: #32323d;
  text-decoration: none;
  display: inline-block;
  padding: 6px 16px;
  font-size: 12px;
  font-weight: 600;
  border: 0;
  border-radius: 999px;
  line-height: normal;
  text-align: center;
  cursor: pointer;
  position: relative;
  text-transform: uppercase;
}
</style>
