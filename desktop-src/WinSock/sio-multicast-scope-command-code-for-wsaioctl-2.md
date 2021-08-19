---
description: Quando o multicast é empregado, geralmente é necessário especificar o escopo sobre o qual a difusão seletiva deve ocorrer.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE o código de comando para WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927365"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ Código de comando do escopo multicast sio para WSAIoctl

Quando o multicast é empregado, geralmente é necessário especificar o *escopo* sobre o qual a difusão seletiva deve ocorrer. O escopo é definido como o número de segmentos de rede roteados a serem cobertos. Um escopo de zero indicaria que a transmissão multicast não seria colocada na conexão, mas poderia ser disseminada entre os soquetes no host local. Um valor de escopo de 1 (o padrão) indica que a transmissão será colocada na conexão, mas não cruzará nenhum roteador. Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados. Observe que isso corresponde ao parâmetro time-to-Live (TTL) no multicast de IP.

A função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é usada para ingressar um nó folha na sessão do MultiPoint. Consulte o seguinte para obter uma discussão sobre como essa função é utilizada.

 

 



