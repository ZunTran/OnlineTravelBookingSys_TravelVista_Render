FROM tomcat:11.0-jdk17

# Xóa app mặc định (Root, Examples) của Tomcat giải phóng RAM cho Render bản Free chạy nhẹ
RUN rm -rf /usr/local/tomcat/webapps/*

# Mở cổng 8080 để Render quét qua và cấp đường link HTTPS
EXPOSE 8080

#Coppy cái file .war dưới máy vào ruột Tomcat trên mây, đổi tên thành ROOT.war để chạy link gốc không cần gõ đuôi tên dự án nữa!
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

# Server chạy vĩnh viễn 24/7
CMD ["catalina.sh", "run"]