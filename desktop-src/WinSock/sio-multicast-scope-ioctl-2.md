---
description: Usando o código de \_ comando SIO MULTICAST \_ SCOPE para especificar o escopo sobre o qual o multicast deve ocorrer.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be65ee600b680805177a44125c03e65e49364ae9008d306349da8f60f9d9de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559684"
---
# <a name="sio_multicast_scope-ioctl"></a>\_IOCTL DE ESCOPO MULTICAST DO SIO \_

Quando o multicast é utilizado, geralmente é necessário especificar o escopo sobre o qual o multicast deve ocorrer. Aqui, o escopo é definido como o número de segmentos de rede roteados a serem cobertos. O código de \_ comando SIO MULTICAST \_ SCOPE para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) é usado para controlar isso. Um escopo de zero indicaria que a transmissão multicast não seria colocada na transmissão, mas poderia ser disseminada entre soquetes dentro do host local. Um valor de escopo de um (o padrão) indica que a transmissão será colocada na transmissão, mas não cruzará nenhum roteador. Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados. Observe que isso corresponde ao parâmetro TTL (vida real) no multicast de IP.

 

 
