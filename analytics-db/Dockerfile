# 
# Unless explicitly acquired and licensed from Licensor under another license, the contents of
# this file are subject to the Reciprocal Public License ("RPL") Version 1.5, or subsequent
# versions as allowed by the RPL, and You may not copy or use this file in either source code
# or executable form, except in compliance with the terms and conditions of the RPL
#
# All software distributed under the RPL is provided strictly on an "AS IS" basis, WITHOUT
# WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, AND LICENSOR HEREBY DISCLAIMS ALL SUCH
# WARRANTIES, INCLUDING WITHOUT LIMITATION, ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
# PARTICULAR PURPOSE, QUIET ENJOYMENT, OR NON-INFRINGEMENT. See the RPL for specific language
# governing rights and limitations under the RPL.
#
# http://opensource.org/licenses/RPL-1.5
#
# Copyright 2012-2016 Open Justice Broker Consortium
# 

# Dockerfile with database layer to support OJB analytics demos

FROM ojbc/mysql

MAINTAINER Open Justice Broker Consortium "http://www.ojbc.org"

WORKDIR /tmp

COPY files/server-config.sh /tmp/
COPY files/ojbc_analytics_demo.sql.gz /tmp/

RUN chmod a+x /tmp/server-config.sh
RUN /tmp/server-config.sh

WORKDIR /usr

CMD ["bin/mysqld_safe", "--user=root"]