---
title: Método getLanguageName IWMPControls3
description: O método getLanguageName retorna o nome da linguagem de áudio com o LCID (identificador de localidade) especificado.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Método getLanguageName Windows Media Player
- Método getLanguageName Windows Media Player interface , IWMPControls3
- Interface IWMPControls3 Windows Media Player , método getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6850bd73c9add044bdb845d17341745c7546918f7824b611ed2f018f66139d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000486"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>Método IWMPControls3::getLanguageName

O **método getLanguageName** retorna o nome da linguagem de áudio com o LCID (identificador de localidade) especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lLangID* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o LCID.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.String** que é o nome da linguagem de áudio.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma suportam apenas uma única saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.audioLanguageCount (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





