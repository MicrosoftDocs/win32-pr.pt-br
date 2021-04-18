---
description: Usando o \_ código de comando do escopo multicast sio \_ para especificar o escopo no qual o multicast deve ocorrer.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763197"
---
# <a name="sio_multicast_scope-ioctl"></a>\_IOCTL do \_ escopo multicast sio

Quando o multicast é empregado, geralmente é necessário especificar o escopo sobre o qual a difusão seletiva deve ocorrer. Aqui, o escopo é definido como o número de segmentos de rede roteados a serem cobertos. O \_ \_ código de comando do escopo multicast sio para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) é usado para controlar isso. Um escopo de zero indicaria que a transmissão multicast não seria colocada na conexão, mas poderia ser disseminada entre os soquetes no host local. Um valor de escopo de um (o padrão) indica que a transmissão será colocada na conexão, mas não vai cruzar nenhum roteador. Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados. Observe que isso corresponde ao parâmetro time-to-Live (TTL) no multicast de IP.

 

 
