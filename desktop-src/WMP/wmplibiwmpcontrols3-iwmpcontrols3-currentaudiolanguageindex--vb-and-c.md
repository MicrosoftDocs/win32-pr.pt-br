---
title: Propriedade IWMPControls3 currentAudioLanguageIndex
description: A propriedade currentAudioLanguageIndex Obtém ou define o índice com base em um que corresponde ao idioma de áudio para reprodução.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Propriedade currentAudioLanguageIndex Windows Media Player
- Propriedade currentAudioLanguageIndex Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751565"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a>Propriedade IWMPControls3:: currentAudioLanguageIndex

A propriedade **currentAudioLanguageIndex** Obtém ou define o índice com base em um que corresponde ao idioma de áudio para reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o índice baseado em um da linguagem.

## <a name="remarks"></a>Comentários

Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.

Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte.

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

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





