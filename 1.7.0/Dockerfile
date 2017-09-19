FROM clojure:boot-2.7.2

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - \
  && apt-get install -y nodejs \
  && apt-get --purge autoremove -y \
  && npm install -g yarn lumo-cljs@1.7.0 --unsafe-perm

CMD ["/usr/bin/lumo"]
