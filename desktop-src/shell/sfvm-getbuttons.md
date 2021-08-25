---
description: Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM_GETBUTTONS mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299641ef45d17a6ad1e4d709c3250abe220e297daedabcb563eeba9dcf56262a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008976"
---
# <a name="sfvm_getbuttons-message"></a>Mensagem GETBUTTONS do SFVM \_

Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[ em\]
</dt> <dd>

Contém dois valores de 16 bits empacotados no parâmetro com a macro [**MAKEWPARAM.**](/windows/win32/api/winuser/nf-winuser-makewparam) A palavra de ordem baixa contém a ID de comando inicial. A palavra de ordem alta contém o número de botões a serem adicionados, conforme especificado na mensagem [**\_ GETBUTTONINFO da SFVM**](sfvm-getbuttoninfo.md) anterior.

</dd> <dt>

*pbtn* \[ out\]
</dt> <dd>

O endereço de uma matriz de estruturas [**TBBUTTON,**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) um para cada botão a ser adicionado à barra de ferramentas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é precedida por uma [**mensagem \_ GETBUTTONINFO SFVM.**](sfvm-getbuttoninfo.md) O objeto de retorno de chamada deve manipular essa mensagem para especificar o número de botões e onde eles devem ser colocados na barra de ferramentas. Dependendo de como o objeto de retorno de chamada responde à mensagem **\_ GETBUTTONINFO SFVM,** os botões especificados pelo parâmetro *pbtn* serão anexados ou anexados aos botões padrão do objeto de exibição de pasta do sistema ou substituirão o conjunto padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
