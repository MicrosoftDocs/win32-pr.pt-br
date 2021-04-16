---
title: Controls. currentAudioLanguage
description: A propriedade currentAudioLanguage especifica ou recupera o identificador de localidade (LCID) do idioma de áudio para reprodução.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls. currentAudioLanguage Windows Media Player
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
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758234"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. currentAudioLanguage

A propriedade **currentAudioLanguage** especifica ou recupera o identificador de localidade (LCID) do idioma de áudio para reprodução.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**longo**).

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.

Ao trabalhar com conteúdo de DVD, a especificação de um LCID fará com que a primeira faixa de áudio disponível com a ID de idioma especificada seja selecionada.

**Windows Media Player 10 Mobile:** Essa propriedade só aceita ou retorna o LCID com neutralidade de idioma (0).

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

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





