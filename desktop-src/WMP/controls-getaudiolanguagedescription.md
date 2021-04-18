---
title: Método Controls. getAudioLanguageDescription
description: O método getAudioLanguageDescription recupera a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- método getAudioLanguageDescription Windows Media Player
- método getAudioLanguageDescription Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760271"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Método Controls. getAudioLanguageDescription

O método **getAudioLanguageDescription** recupera a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) especificando o índice de idioma de áudio baseado em um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um valor de **cadeia de caracteres** .

## <a name="remarks"></a>Comentários

Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.

Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

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

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





