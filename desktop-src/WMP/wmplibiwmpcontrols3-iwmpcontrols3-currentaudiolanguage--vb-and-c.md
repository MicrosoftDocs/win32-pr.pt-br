---
title: Propriedade IWMPControls3 currentAudioLanguage
description: A propriedade currentAudioLanguage Obtém ou define o identificador de localidade (LCID) do idioma de áudio para reprodução.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Propriedade currentAudioLanguage Windows Media Player
- Propriedade currentAudioLanguage Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765749"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>Propriedade IWMPControls3:: currentAudioLanguage

A propriedade **currentAudioLanguage** Obtém ou define o identificador de localidade (LCID) do idioma de áudio para reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o LCID do idioma de áudio.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.

Ao trabalhar com conteúdo de DVD, a especificação de um LCID fará com que a primeira faixa de áudio disponível com a ID de idioma especificada seja selecionada.

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

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





