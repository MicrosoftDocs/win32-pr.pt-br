---
title: IAgentBalloon getabilited
description: IAgentBalloon getabilited
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292806"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon:: getabilited

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Recupera o valor da propriedade [**Enabled**](enabled-property.md) para um balão de palavra.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

O endereço de uma variável que recebe **true** quando a palavra balão estiver habilitada e **false** quando for desabilitada.

</dd> </dl>

O servidor Microsoft Agent exibe automaticamente o balão de palavras para saída falada, a menos que esteja desabilitada. O balão de palavras pode ser desabilitado para um caractere no editor de caracteres do Microsoft Agent ou (pelo usuário) para todos os caracteres na folha de propriedades do Microsoft Agent. Se o usuário desabilitar a palavra balão, o cliente não poderá restaurá-la.

 

 




