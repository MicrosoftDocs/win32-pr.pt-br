---
title: Método getAudioLanguageDescription de IWMPControls3
description: O método getAudioLanguageDescription retorna a descrição da linguagem de áudio correspondente ao índice baseado em um especificado.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- Método getAudioLanguageDescription Windows Media Player
- Método getAudioLanguageDescription Windows Media Player interface , IWMPControls3
- Interface IWMPControls3 Windows Media Player , método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1172fd119671a8452ac581d3c3a27efd890456cec98f1ef8d6e61340a54c4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861866"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>Método IWMPControls3::getAudioLanguageDescription

O **método getAudioLanguageDescription** retorna a descrição da linguagem de áudio correspondente ao índice baseado em um especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* \[ Em\]
</dt> <dd>

Um **System.Int32 que** é o índice de linguagem de áudio baseado em um.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.String** que é a descrição da linguagem de áudio.

## <a name="remarks"></a>Comentários

Para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma suportam apenas uma única saída.

Use a **propriedade audioLanguageCount** para obter o número de linguagens de áudio com suporte e, em seguida, acesse uma linguagem de áudio individualmente usando um índice baseado em um.

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

[**IWMPControls3.currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





