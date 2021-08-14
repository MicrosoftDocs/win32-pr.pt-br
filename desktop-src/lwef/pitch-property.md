---
title: Propriedade Pitch
description: Propriedade Pitch
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
# <a name="pitch-property"></a>Propriedade Pitch

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descrição** 
</dt> <dd>

Retorna um inteiro Longo para a configuração de tom de TTS (saída de fala) do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Apresentação_*

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente aos caracteres configurados para a saída do TTS. Se o caractere não dá suporte à saída TTS, essa propriedade retorna zero (0).

Embora seu aplicativo não possa gravar  esse valor, você pode incluir marcas pit (tom) no texto de saída que aumentarão temporariamente o tom de um enunciado específico. No entanto, usar a **marca Pit** para alterar o tom não alterará a **configuração da** propriedade Pitch. Para obter mais informações, consulte [Marcas de saída de fala](pit-tag.md).

 

 




