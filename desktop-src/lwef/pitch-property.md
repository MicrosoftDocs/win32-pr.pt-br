---
title: Propriedade pitch
description: Propriedade pitch
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475405"
---
# <a name="pitch-property"></a>Propriedade pitch

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Ndescrição** 
</dt> <dd>

Retorna um inteiro longo para a configuração de Tom de saída de fala (TTS) do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente ***. Caracteres ("**_characterid_*_"). Pitch_*

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade só se aplica a caracteres configurados para saída de TTS. Se o caractere não oferecer suporte à saída de TTS, essa propriedade retornará zero (0).

Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas **Pit** (Pitch) no texto de saída que aumentarão temporariamente o timbre de um determinado expressão. No entanto, usar a marca **Pit** para alterar a densidade não alterará a configuração da propriedade **pitch** . Para obter mais informações, consulte [marcas de saída de fala](pit-tag.md).

 

 




