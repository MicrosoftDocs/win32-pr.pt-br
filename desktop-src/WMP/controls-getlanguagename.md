---
title: Método Controls. getLanguageName
description: O método getLanguageName recupera o nome do idioma de áudio com o LCID (identificador de localidade) especificado.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- método getLanguageName do Windows Media Player
- método getLanguageName Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783619"
---
# <a name="controlsgetlanguagename-method"></a>Método Controls. getLanguageName

O método **getLanguageName** recupera o nome do idioma de áudio com o LCID (identificador de localidade) especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LCID* \[ em\]
</dt> <dd>

**Número** (**longo**) que especifica o LCID.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.

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

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





