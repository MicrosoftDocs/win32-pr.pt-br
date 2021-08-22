---
description: A classe de dispositivo TAPI/terminal consiste nos dispositivos de telefone associados a cada terminal em uma linha ou ao terminal em cada linha associada a um dispositivo de telefone. Você acessa esses dispositivos usando o dispositivo de linha TAPI ou as funções de dispositivo de telefone.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1026087415e09e38c9b8af903145f13f56ccf426f2355e46bd0bb5f5ddadc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860668"
---
# <a name="tapiterminal"></a>TAPI/terminal

A classe de dispositivo TAPI/terminal consiste nos dispositivos de telefone associados a cada terminal em uma linha ou ao terminal em cada linha associada a um dispositivo de telefone. Você acessa esses dispositivos usando o dispositivo de [linha](line-device-functions.md) TAPI ou as [funções de dispositivo de telefone](phone-device-functions.md).

A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

O membro **adwDeviceId** é uma matriz de identificadores de dispositivo de telefone. Há um elemento de matriz para cada terminal especificado pelo membro **dwNumTerminals** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) do dispositivo de linha especificado. Cada elemento Especifica o identificador do dispositivo de telefone associado ao terminal correspondente na linha. Se não houver nenhum dispositivo telefônico associado a um terminal, o elemento será definido como – 1 (0xFFFFFFFF).

A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

O membro **adwTerminalID** é uma matriz de identificadores de terminal. Há um elemento de matriz para cada identificador de dispositivo de linha especificado pela função [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) . Cada elemento de matriz contém o identificador de terminal associado ao dispositivo de telefone para o dispositivo de linha especificado. Se não houver nenhum dispositivo telefônico, o elemento será definido como – 1 (0xFFFFFFFF). Os identificadores de terminal variam em valor de zero a um menor que o número especificado pelo membro **dwNumTerminals** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .

 

 



