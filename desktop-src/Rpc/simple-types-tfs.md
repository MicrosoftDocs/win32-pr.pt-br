---
title: Tipos simples
description: Todos os tipos simples são representados por um único caractere de formato que indica o tipo por seu nome.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925156"
---
# <a name="simple-types"></a>Tipos simples

Todos os tipos simples são representados por um único caractere de formato que indica o tipo por seu nome. Isso inclui todos os tipos numéricos e outros tipos de IDL especiais. A lista é a seguinte:

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

Os tipos SMALL, WCHAR, HYPER, \_ status \_ de erro T, \_ \_ INT3264 são intrínsecos a MIDL com interpretações de RPC especiais. Os tipos INT e \_ \_ Int32 mapeiam para FC \_ longo, não assinados int e não assinados para o mapa \_ \_ INT32 para o FC \_ ULong, \_ \_ Int64 e \_ \_ para o mapa Int64 não assinado para FC \_ Hyper.

Os \_ \_ tipos INT128, FLOAT128 e FLOAT80 não têm suporte.

 

 




