---
title: IAgentAudioOutputProperties getabilited
description: IAgentAudioOutputProperties getabilited
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005476"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>IAgentAudioOutputProperties:: getabilited

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Recupera um valor que indica se a saída de fala de caractere está habilitada.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Endereço de uma variável que recebe **true** se a saída de fala estiver habilitada no momento e **false** se estiver desabilitada.

</dd> </dl>

Como essa configuração afeta a saída falada (TTS e arquivo de som) para todos os caracteres, somente o usuário pode alterar essa propriedade na folha de propriedades do Microsoft Agent.

 

 




