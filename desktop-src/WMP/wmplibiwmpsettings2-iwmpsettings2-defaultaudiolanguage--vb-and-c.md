---
title: Propriedade IWMPSettings2 defaultAudioLanguage
description: A propriedade defaultAudioLanguage Obtém o LCID (identificador de localidade) do idioma de áudio padrão especificado em Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Windows Media Player da propriedade defaultAudioLanguage
- propriedade defaultAudioLanguage Windows Media Player, interface IWMPSettings2
- Windows Media Player de interface IWMPSettings2, propriedade defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331096"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2: Propriedade efaultAudioLanguage de:d

A propriedade **defaultAudioLanguage** Obtém o LCID (identificador de localidade) do idioma de áudio padrão especificado em Windows Media Player.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o LCID.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





