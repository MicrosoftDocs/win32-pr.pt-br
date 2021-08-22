---
title: Escolhendo uma sequência de protocolo
description: As práticas recomendadas para escolher uma sequência de protocolo envolvem o uso de ncacn ip tcp e \_ \_ ncalrpc, não ncacn \_ np, ncacn \_ spx e ncadg \_ \ .
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932219"
---
# <a name="choosing-a-protocol-sequence"></a>Escolhendo uma sequência de protocolo

**Melhor prática:** Use [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) ao fazer uma chamada remota. Use [**ncalrpc para**](/windows/desktop/Midl/ncalrpc) chamadas locais. Não use [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ spx**](/windows/desktop/Midl/ncacn-spx)ou qualquer uma das sequências de protocolo **ncadg; \_ \*** elas são menos eficientes e têm funcionalidades inferiores.

 

 