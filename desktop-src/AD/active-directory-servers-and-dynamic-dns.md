---
title: Servidores de Active Directory e DNS dinâmico
description: Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory de DNS dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9828a2d6d14d862e98d3c5c4129bbc70f5c411
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880062"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Servidores de Active Directory e DNS dinâmico

Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio. Os servidores de Active Directory são publicados usando os registros de recursos de serviço (SRV RRs) no DNS. O RR SRV é um registro DNS usado para mapear o nome de um serviço para o endereço de um servidor que oferece o serviço. O nome de um RR SRV está neste formato:


```C++
<service>.<protocol>.<domain>
```



Os servidores de Active Directory oferecem o serviço LDAP sobre o protocolo TCP para que os nomes publicados sejam "LDAP. TCP. &lt; domínio &gt; ". Portanto, o RR SRV para fabrikam.com é "ldap.tcp.fabrikam.com". Dados adicionais sobre o RR SRV indicam a prioridade e o peso do servidor, permitindo que os clientes escolham o melhor servidor para suas necessidades.

Quando um servidor de Active Directory é instalado, ele usa o DNS dinâmico para publicar a si mesmo. Como os endereços TCP/IP estão sujeitos a alterações, os servidores verificam periodicamente seus registros para certificar-se de que estão corretos e atualizá-los se necessário.

O DNS dinâmico é uma adição recente ao padrão de DNS. O DNS dinâmico define um protocolo para atualizar dinamicamente um servidor DNS com novos dados. Antes do DNS dinâmico, os administradores eram solicitados a configurar manualmente os registros armazenados por servidores DNS.

 

 




