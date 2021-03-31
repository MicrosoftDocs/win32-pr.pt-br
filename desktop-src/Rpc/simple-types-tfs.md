---
title: Tipos simples
description: Todos os tipos simples são representados por um único caractere de formato que indica o tipo por seu nome.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe123ca7c06a0522a139dc0cca8a9e24d1d585d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636650"
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

 

 




