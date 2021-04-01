---
title: Escolhendo uma sequência de protocolo
description: As práticas recomendadas para escolher uma sequência de protocolo envolvem o uso de ncacn \_ IP \_ TCP e Ncalrpc, não ncacn \_ NP, ncacn \_ SPX e ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008081"
---
# <a name="choosing-a-protocol-sequence"></a>Escolhendo uma sequência de protocolo

**Prática recomendada:** Use [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) ao fazer uma chamada remota. Use [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) para chamadas locais. Não use [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)ou qualquer uma das sequências de protocolo **ncadg \_ \*** ; elas são menos eficientes e têm recursos inferiores.

 

 