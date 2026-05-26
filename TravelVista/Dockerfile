FROM tomcat:10.1-jdk17

# Xóa sạch các app mặc định của Tomcat để tránh tranh chấp cổng
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy file .war được build từ NetBeans vào làm app chạy chính (ROOT.war)
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

# Mở cổng 8080 cho Railway vào quét sóng
EXPOSE 8080

# Chạy Tomcat trực tiếp, sạch sẽ, không dùng lệnh sed lỗi thời nữa
CMD ["catalina.sh", "run"]
