---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976446"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Reproduz a animação de estado **gesturing** associada com base no local especificado.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x do local especificado em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y do local especificado em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID de solicitação **GestureAt** .

</dd> </dl>

O servidor determina automaticamente e reproduz a animação gesturing apropriada com base na posição atual do caractere e no local especificado. Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](iagentcharacter--prepare.md) para garantir que as animações estejam disponíveis antes de chamar esse método.

 

 




