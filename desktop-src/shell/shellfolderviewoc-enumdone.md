---
description: Indica que o objeto ShellFolderView terminou de enumerar o conteúdo da pasta.
title: Evento ShellFolderViewOC. EnumDone (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989060"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC. EnumDone

Indica que o objeto [**ShellFolderView**](shellfolderview.md) terminou de enumerar o conteúdo da pasta.

## <a name="syntax"></a>Sintaxe


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Parâmetros

Este manipulador de eventos não tem parâmetros.

## <a name="remarks"></a>Comentários

O objeto [**ShellFolderView**](shellfolderview.md) deve enumerar o conteúdo de uma pasta para poder exibi-la. Com pastas grandes ou localizadas em um sistema remoto, esse processo pode levar até vários minutos. Durante esse tempo, um gráfico de lanterna animada é exibido para indicar ao usuário que o processamento está sob o caminho. Depois que a enumeração for concluída, o evento **EnumDone** será acionado e o gráfico de lanterna será substituído pelo conteúdo da pasta.

Forneça o código de manipulação de eventos para esse evento, conforme mostrado aqui.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




