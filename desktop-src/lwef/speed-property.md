---
title: Propriedade Speed
description: Propriedade Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798405"
---
# <a name="speed-property"></a>Propriedade Speed

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um inteiro longo que especifica a velocidade atual da saída de fala do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Rápida**

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade retorna a configuração de velocidade de saída de fala atual para o caractere. Para caracteres que usam a saída de TTS, a propriedade retorna a configuração de saída de TTS real para o caractere. Se a TTS não estiver habilitada ou o caractere não oferecer suporte à saída de TTS, a configuração refletirá a configuração de usuário para a velocidade de saída.

Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas **SPD** (Speed) no texto de saída que acelerará temporariamente a saída para um determinado expressão. No entanto, usar a marca **SPD** para alterar a saída falada do caractere não afeta a configuração da propriedade **Speed** . Para obter mais informações, consulte [marcas de saída de fala](microsoft-agent-speech-output-tags.md).

 

 




