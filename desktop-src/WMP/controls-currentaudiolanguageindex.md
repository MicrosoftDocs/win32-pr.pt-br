---
title: Controls. currentAudioLanguageIndex
description: A propriedade currentAudioLanguageIndex especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls. currentAudioLanguageIndex Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789570"
---
# <a name="controlscurrentaudiolanguageindex"></a>Controls. currentAudioLanguageIndex

A propriedade **currentAudioLanguageIndex** especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**longo**).

## <a name="remarks"></a>Comentários

Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.

Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte.

**Windows Media Player 10 Mobile:** Essa propriedade só aceita ou retorna 0.

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

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





