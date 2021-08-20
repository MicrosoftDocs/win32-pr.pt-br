---
title: Servidores de Active Directory e DNS dinâmico
description: Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory de DNS dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9508bd571cf60d3801cc5708276ff9399494e354ee3559efd0a3ffa0b96836a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025196"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Servidores de Active Directory e DNS dinâmico

Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio. Os servidores de Active Directory são publicados usando os registros de recursos de serviço (SRV RRs) no DNS. O RR SRV é um registro DNS usado para mapear o nome de um serviço para o endereço de um servidor que oferece o serviço. O nome de um RR SRV está neste formato:


```C++
<service>.<protocol>.<domain>
```



Os servidores de Active Directory oferecem o serviço LDAP sobre o protocolo TCP para que os nomes publicados sejam "LDAP. TCP. <domain> ". Portanto, o RR SRV para fabrikam.com é "ldap.tcp.fabrikam.com". Dados adicionais sobre o RR SRV indicam a prioridade e o peso do servidor, permitindo que os clientes escolham o melhor servidor para suas necessidades.

Quando um servidor de Active Directory é instalado, ele usa o DNS dinâmico para publicar a si mesmo. Como os endereços TCP/IP estão sujeitos a alterações, os servidores verificam periodicamente seus registros para certificar-se de que estão corretos e atualizá-los se necessário.

O DNS dinâmico é uma adição recente ao padrão de DNS. O DNS dinâmico define um protocolo para atualizar dinamicamente um servidor DNS com novos dados. Antes do DNS dinâmico, os administradores eram solicitados a configurar manualmente os registros armazenados por servidores DNS.

 

 




