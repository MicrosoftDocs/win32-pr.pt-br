---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364506"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




