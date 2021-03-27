---
description: 'Permite que o objeto de retorno de chamada adicione botões à barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETBUTTONINFO (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968069"
---
# <a name="sfvm_getbuttoninfo-message"></a>\_Mensagem SFVM GETBUTTONINFO

Permite que o objeto de retorno de chamada adicione botões à barra de ferramentas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptbinfo* \[ fora\]
</dt> <dd>

O endereço de uma estrutura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) que especifica o número de botões e como eles devem ser adicionados à barra de ferramentas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os botões podem ser acrescentados ou anexados aos botões de objeto de exibição da pasta do sistema padrão ou ser exibidos no lugar dos botões padrão. Essa mensagem é seguida por uma mensagem [**SFVM \_ getbuttons**](sfvm-getbuttons.md) que recupera as informações relacionadas às especificações do botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
