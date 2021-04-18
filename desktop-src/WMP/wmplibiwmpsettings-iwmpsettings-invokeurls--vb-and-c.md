---
title: Propriedade IWMPSettings invokeURLs
description: A propriedade invokeURLs Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Propriedade invokeURLs Windows Media Player
- Propriedade invokeURLs Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798168"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Propriedade IWMPSettings:: invokeURLs

A propriedade **invokeURLs** Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor **System. booliano** que indica se os eventos de URL devem iniciar um navegador da Web. O padrão é **true**.

## <a name="remarks"></a>Comentários

Os arquivos de mídia digital e os fluxos podem conter comandos de script de URL. Quando um comando de script de URL é enviado ao controle do Windows Media Player, ele é passado primeiro para o manipulador de eventos **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , independentemente do valor recuperado por **invokeURLs**. Após o **\_ WMPOCXEvents \_ ScriptCommandEvent** sair, o Windows Media Player verifica **invokeURLs** para determinar se o navegador da Web padrão deve ser iniciado com a URL. Você pode exibir URLs seletivamente, verificando-as em **\_ WMPOCXEvents \_ ScriptCommandEvent** e configurando **invokeURLs** conforme desejado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





