---
description: Indica que o objeto ShellFolderView concluiu a enumeração do conteúdo da pasta.
title: Evento ShellFolderViewOC.EnumDone (Shldisp.h)
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
ms.openlocfilehash: c725a61a6711dab22d50b774cb02556916dae802a66008a48721d7311e163bce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660636"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC.EnumDone

Indica que o [**objeto ShellFolderView**](shellfolderview.md) concluiu a enumeração do conteúdo da pasta.

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

Esse manipulador de eventos não tem parâmetros.

## <a name="remarks"></a>Comentários

O [**objeto ShellFolderView**](shellfolderview.md) deve enumerar o conteúdo de uma pasta antes de poder exibi-lo. Com pastas grandes ou localizadas em um sistema remoto, esse processo pode levar até vários minutos. Durante esse tempo, um gráfico de luzes animadas é exibido para indicar ao usuário que o processamento está em andamento. Depois que a enumeração for concluída, o evento **EnumDone** será acionado e o gráfico de luzes será substituído pelo conteúdo da pasta.

Forneça o código de manipulação de eventos para esse evento, conforme mostrado aqui.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




