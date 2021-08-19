---
title: Propriedade IWMPControls3 currentAudioLanguage
description: A propriedade currentAudioLanguage obtém ou define o LCID (identificador de localidade) da linguagem de áudio para reprodução.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- propriedade currentAudioLanguage Windows Media Player
- propriedade currentAudioLanguage Windows Media Player interface , IWMPControls3
- Interface IWMPControls3 Windows Media Player , propriedade currentAudioLanguage
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
ms.openlocfilehash: 1e1a4f668cec560528270d52a2abe4777ce32d3ceb38ce21345342ef87866c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115873"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>Propriedade IWMPControls3::currentAudioLanguage

A **propriedade currentAudioLanguage** obtém ou define o LCID (identificador de localidade) da linguagem de áudio para reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o LCID da linguagem de áudio.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para Windows conteúdo baseado em mídia, as propriedades e os métodos relacionados à seleção de idioma suportam apenas uma única saída.

Ao trabalhar com conteúdo de DVD, especificar um LCID fará com que a primeira faixa de áudio disponível tenha a ID de idioma especificada selecionada.

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

[**IWMPControls3.getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





