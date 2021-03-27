---
description: 'Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Mensagem de SFVM_GETBUTTONS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829220"
---
# <a name="sfvm_getbuttons-message"></a>\_Mensagem de GETbotãors do SFVM

Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[\]
</dt> <dd>

Contém valores de 2 16 bits incluídos no parâmetro com a macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) . A palavra de ordem inferior contém a ID de comando inicial. A palavra de ordem superior contém o número de botões a serem adicionados, conforme especificado na mensagem [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) anterior.

</dd> <dt>

*pbtn* \[ fora\]
</dt> <dd>

O endereço de uma matriz de estruturas [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , uma para cada botão a ser adicionado à barra de ferramentas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é precedida por uma mensagem [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) . O objeto de retorno de chamada deve lidar com essa mensagem para especificar o número de botões e onde eles devem ser colocados na barra de ferramentas. Dependendo de como o objeto de retorno de chamada responde à mensagem **SFVM \_ GETBUTTONINFO** , os botões especificados pelo parâmetro *pbtn* serão acrescentados ou anexados aos botões padrão do objeto de exibição da pasta do sistema ou substituirão o conjunto padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
