---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781092"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Recupera a configuração de densidade de saída TTS do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

Endereço de uma variável que recebe a configuração de densidade de TTS atual do caractere em Hertz.

</dd> </dl>

Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas de densidade no texto de saída que aumentarão temporariamente a inclinação de um determinado expressão. Esse método se aplica somente a caracteres configurados para saída de TTS. Se o mecanismo de síntese de fala (TTS) não estiver habilitado (ou instalado) ou se o caractere não oferecer suporte à saída de TTS, esse método retornará zero (0).

 

 




