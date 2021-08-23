---
title: Propriedade invokeURLs de IWMPSettings
description: A propriedade invokeURLs obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Propriedade invokeURLs Windows Media Player
- A propriedade invokeURLs Windows Media Player interface , IWMPSettings
- Interface IWMPSettings Windows Media Player propriedade , invokeURLs
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
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053424"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Propriedade IWMPSettings::invokeURLs

A **propriedade invokeURLs** obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um **valor System.Boolean** que indica se os eventos de URL devem iniciar um navegador da Web. O padrão é **true**.

## <a name="remarks"></a>Comentários

Arquivos de mídia digital e fluxos podem conter comandos de script de URL. Quando um comando de script de URL é enviado para o controle Windows Media Player, ele é passado primeiro para o manipulador de eventos **\_ \_ ScriptCommandEventS WMPOCXEvent do AxWindowsMediaPlayer,** independentemente do valor recuperado por **invokeURLs.** Após **\_ o WMPOCXEvents \_ ScriptCommandEvent** sair, o Windows Media Player verifica **invokeURLs** para determinar se o navegador da Web padrão deve ser lançado com a URL. Você pode exibir as URLs seletivamente verificando-as em **\_ WMPOCXEvents \_ ScriptCommandEvent** e definindo **invokeURLs** conforme desejado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





