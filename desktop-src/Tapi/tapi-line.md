---
description: A classe de dispositivo TAPI/linha consiste em todos os dispositivos de linha. Você acessa esses dispositivos usando as funções de linha TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56478f43d1055d7bf2a382bc84611360675da97e506812a1806df4beca0aeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760728"
---
# <a name="tapiline"></a>TAPI/linha

A classe de dispositivo TAPI/linha consiste em todos os dispositivos de linha. Você acessa esses dispositivos usando as funções de linha TAPI.

A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

O membro **dwDeviceId** é o identificador do dispositivo de linha associado ao identificador de linha fornecido pelo [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) também preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **dwStringFormat** como StringFormat \_ Binary e acrescentando esse membro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

O membro **adwDeviceIds** é uma matriz que contém os identificadores de todos os dispositivos de linha associados ao dispositivo telefônico. Se não houver nenhum dispositivo de linha associado, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) retornará o \_ valor de INVALDEVICECLASS PHONEERR.

 

 



