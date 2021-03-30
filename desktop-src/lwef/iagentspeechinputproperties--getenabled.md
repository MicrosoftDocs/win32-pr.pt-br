---
title: IAgentSpeechInputProperties getabilited
description: IAgentSpeechInputProperties getabilited
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634737"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties:: getabilited

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

Recupera um valor que indica se o mecanismo de reconhecimento de fala instalado está habilitado.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Endereço de uma variável que recebe **true** se o mecanismo de fala estiver habilitado no momento e **false** se estiver desabilitado.

</dd> </dl>

 

 




