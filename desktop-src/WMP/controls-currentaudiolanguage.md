---
title: Controls.currentAudioLanguage
description: A propriedade currentAudioLanguage especifica ou recupera o LCID (identificador de localidade) da linguagem de áudio para reprodução.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls.currentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750608"
---
# <a name="controlscurrentaudiolanguage"></a>Controls.currentAudioLanguage

A **propriedade currentAudioLanguage** especifica ou recupera o LCID (identificador de localidade) da linguagem de áudio para reprodução.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um número de **leitura/gravação** (**longo).**

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma só são suportados por uma única saída.

Ao trabalhar com conteúdo de DVD, especificar um LCID fará com que a primeira faixa de áudio disponível tenha a ID de idioma especificada selecionada.

**Windows Media Player 10 Mobile:** Essa propriedade só aceita ou retorna o LCID neutro em idioma (0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





