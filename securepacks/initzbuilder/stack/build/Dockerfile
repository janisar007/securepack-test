# Define the base image
FROM initializbuildpacks/initz-base:latest
 
# Switch to the root user to install packages
USER root
 
# Update package database and install dependencies
RUN apk update && \
    apk del libcrypt1  && \
    apk add \
        apk-tools \
        binutils \
        glibc \
        glibc-dev\
        glibc-locale-posix \
        isl \
        ld-linux \
        libatomic \
        libbrotlicommon1 \
        libbrotlidec1 \
        libcrypt1 \
        libgcc \
        libgo \
        libcrypto3 \
        libcurl-openssl4 \
        libffi \
        build-base \
        make \
        libgomp \
        libidn2\
        libnghttp2-14 \
        libpcre2-8-0 \
        libpsl \
        libstdc++\
        libstdc++-dev \
        libunistring \
        libxcrypt-dev \
        linux-headers\
        mpc \
        mpfr \
        ncurses \
        ncurses-terminfo-base \
        nss-db \
        nss-hesiod \
        openssl-config \
        posix-cc-wrappers \
        ruby-3.3 \
        ruby-3.3-dev \
        ruby3.3-bundler \
        wget\
        wolfi-baselayout \
        ca-certificates-bundle \
        curl \
        git \
        jq \
        libexpat1 \
        py3-pip \
        gmp \
        libssl3 \
        yaml \
        openssl \
        openssl-dev \
        pkgconf \
        tzdata \
        zlib \
        zlib-dev \
        xz \
        xdg-utils \
        libstdc++ \
        bash \
        libffi-dev \
        python3-dev \
        libfontconfig1 \
        fontconfig \
        ttf-dejavu \
        libxcrypt \
        libxml2 \
        sqlite \
        pcre \
        libunwind \
        wolfi-base \
        busybox 
       
 
# Create symbolic link for libpcre
RUN ln -s /usr/lib/libpcre.so.1 /usr/lib/libpcre.so.3
 
# Switch back to the non-root user
USER cnb
 
# Set required CNB target information
LABEL io.buildpacks.base.distro.name="wolfi"
LABEL io.buildpacks.base.distro.version="20230201"
 
LABEL io.buildpacks.stack.id="Initializ Distroless Stack"
 
ENV CNB_STACK_ID="Initializ Distroless Stack"
