---
title: Método IWMPControls3 getAudioLanguageDescription
description: O método getAudioLanguageDescription retorna a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- método getAudioLanguageDescription Windows Media Player
- método getAudioLanguageDescription Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, método getAudioLanguageDescription
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
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749519"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>Método IWMPControls3:: getAudioLanguageDescription

O método **getAudioLanguageDescription** retorna a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.

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

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de idioma de áudio baseado em um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é a descrição do idioma de áudio.

## <a name="remarks"></a>Comentários

Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.

Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





