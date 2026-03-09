<template>
  <div id="contactPage">
    <div class="page-header">
      <h1>联系我们</h1>
      <p class="subtitle">如果您有任何问题或需求，请通过以下方式联系我们</p>
    </div>
    <a-card class="contact-card">
      <div class="contact-content">
        <div class="contact-icon">
          <a-avatar size="80" :icon="h(MessageOutlined)" style="background-color: #1890ff;" />
        </div>
        <div class="contact-info">
          <a-descriptions :column="1" size="large">
            <a-descriptions-item label="QQ">
              <a-text strong style="font-size: 20px; color: #1890ff;">2532371880</a-text>
            </a-descriptions-item>
            <a-descriptions-item label="服务时间">
              <a-text>周一至周五 9:00-18:00</a-text>
            </a-descriptions-item>
            <a-descriptions-item label="服务内容">
              <a-text>空间升级、技术支持、问题反馈</a-text>
            </a-descriptions-item>
          </a-descriptions>
        </div>
      </div>
    </a-card>
  </div>
</template>

<script setup lang="ts">
import { h } from 'vue';
import { MessageOutlined } from '@ant-design/icons-vue';
</script>

<style scoped>
#contactPage {
  max-width: 800px;
  margin: 0 auto;
  padding: 40px 24px;
}

.page-header {
  text-align: center;
  margin-bottom: 40px;
}

.page-header h1 {
  font-size: 32px;
  font-weight: bold;
  color: #1890ff;
  margin-bottom: 12px;
}

.subtitle {
  font-size: 16px;
  color: #666;
  margin: 0;
}

.contact-card {
  background: linear-gradient(135deg, #f0f8ff 0%, #ffffff 100%);
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
  padding: 32px;
  transition: all 0.3s ease;
}

.contact-card:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
  transform: translateY(-2px);
}

.contact-content {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;
}

.contact-icon {
  flex-shrink: 0;
}

.contact-info {
  flex: 1;
  min-width: 0;
}

@media (max-width: 768px) {
  .contact-content {
    flex-direction: column;
    text-align: center;
  }
  
  .page-header h1 {
    font-size: 24px;
  }
  
  .contact-card {
    padding: 24px;
  }
}
</style>