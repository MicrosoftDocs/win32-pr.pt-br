---
title: Método Controls.getAudioLanguageDescription
description: O método getAudioLanguageDescription recupera a descrição da linguagem de áudio correspondente ao índice baseado em um especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Método getAudioLanguageDescription Windows Media Player
- Método getAudioLanguageDescription Windows Media Player classe , Controls
- Classe Controls Windows Media Player , método getAudioLanguageDescription
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
ms.openlocfilehash: 29aa5f7b5c0ad72ff13b571505283b243bd62d79ebc4339717ed8283cccb2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997496"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Método Controls.getAudioLanguageDescription

O **método getAudioLanguageDescription** recupera a descrição da linguagem de áudio correspondente ao índice baseado em um especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

**Número** (**longo**) especificando o índice de linguagem de áudio baseado em um.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um valor **string.**

## <a name="remarks"></a>Comentários

Para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma só são suportados por uma única saída.

Use a **propriedade audioLanguageCount** para obter o número de linguagens de áudio com suporte e, em seguida, acesse uma linguagem de áudio individualmente usando um índice baseado em um.

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

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

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





