---
title: Método Controls. getAudioLanguageID
description: O método getAudioLanguageID recupera o LCID (identificador de localidade) para um índice de idioma de áudio especificado.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- Windows Media Player do método getAudioLanguageID
- método getAudioLanguageID Windows Media Player, classe Controls
- classe Controls Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2352162d810ca75aeeee6db1c3d59c297b85414be46a365909c4ed56af179f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119334"
---
# <a name="controlsgetaudiolanguageid-method"></a>Método Controls. getAudioLanguageID

O método **getAudioLanguageID** recupera o LCID (identificador de localidade) para um índice de idioma de áudio especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que especifica o índice de idioma de áudio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna o LCID com neutralidade de idioma (0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls. audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





