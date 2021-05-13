---
description: Encaminha os eventos acionados por um objeto ShellFolderView especificado para manipuladores de eventos ShellFolderViewOC correspondentes.
title: Objeto ShellFolderViewOC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840867"
---
# <a name="shellfolderviewoc-object"></a>Objeto ShellFolderViewOC

Encaminha os eventos acionados por um objeto [**ShellFolderView**](shellfolderview.md) especificado para manipuladores de eventos **ShellFolderViewOC** correspondentes.

## <a name="members"></a>Membros

O objeto **ShellFolderViewOC** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)

### <a name="events"></a>Eventos

O objeto **ShellFolderViewOC** tem esses eventos.



| Evento                                                          | Descrição                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | Indica que o objeto [**ShellFolderView**](shellfolderview.md) terminou de enumerar o conteúdo da pasta.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Indica que o estado de seleção de um ou mais itens na exibição foi alterado.<br/>                                     |



 

### <a name="methods"></a>Métodos

O objeto **ShellFolderViewOC** tem esses métodos.



| Método                                                   | Descrição                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | Encaminha os eventos do objeto [**ShellFolderView**](shellfolderview.md) especificado para o manipulador de eventos **ShellFolderViewOC** correspondente.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto [**ShellFolderView**](shellfolderview.md) aciona dois eventos, [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), que normalmente são manipulados por aplicativos. No entanto, alguns aplicativos devem manipular eventos de uma série de objetos **ShellFolderView** . Por exemplo, um aplicativo pode hospedar um controle WebBrowser que permite aos usuários navegar por uma série de pastas. Cada pasta tem seu próprio objeto **ShellFolderView** com seus eventos associados. Lidar com esses eventos pode ser difícil.

O objeto **ShellFolderViewOC** simplifica a manipulação de eventos para esses cenários. Ele permite que os aplicativos manipulem eventos para todos os objetos [**ShellFolderView**](shellfolderview.md) com um único par de manipuladores de eventos **ShellFolderViewOC** . Cada vez que o usuário navega para uma nova pasta, o aplicativo passa o objeto **ShellFolderView** associado para o objeto **ShellFolderViewOC** chamando [**SetFolderView**](shellfolderviewoc-setfolderview.md). Em seguida, quando [**um evento EnumDone**](shellfolderviewoc-enumdone.md) ou [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) é acionado, o objeto **ShellFolderViewOC** encaminha o evento para seu próprio manipulador para processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




