FROM streamreasoning/stream-server:latest

ADD ./obda/experiments ./obda/experiments
ADD ./default.properties ./default.properties
ADD ./postgres.properties ./postgres.properties
ADD ./virtual-entrypoint.sh ./virtual-entrypoint.sh
RUN chmod u+x ./virtual-entrypoint.sh

RUN ls ./obda/experiments/
RUN head --lines=20 ./obda/experiments/citybench.owl

ADD ./wait-for-it.sh ./wait-for-it.sh
RUN chmod u+x ./wait-for-it.sh

ENTRYPOINT ["./virtual-entrypoint.sh"]
CMD ["default.properties"]