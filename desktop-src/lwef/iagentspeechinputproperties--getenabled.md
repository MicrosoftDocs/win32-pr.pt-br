---
title: IAgentSpeechInputProperties getabilited
description: IAgentSpeechInputProperties getabilited
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404bd6f0348487c8e039c247f5a9368359133be9e3df76b884115679a2961a97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114666"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties:: getabilited

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




