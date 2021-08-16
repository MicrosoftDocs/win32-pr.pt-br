---
description: Permite que o objeto de retorno de chamada especifique uma cadeia de caracteres de texto de dica de ferramenta para itens de menu ou botões de barra de ferramentas. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: SFVM_GETTOOLTIPTEXT mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350d1f772cd78c97f7b57b47084c761808583dfe5396fafcdad336291a3a717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858218"
---
# <a name="sfvm_gettooltiptext-message"></a>Mensagem GETTOOLTIPTEXT de SFVM \_

Permite que o objeto de retorno de chamada especifique uma cadeia de caracteres de texto de dica de ferramenta para itens de menu ou botões de barra de ferramentas. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd \_ cchMax* \[ em\]
</dt> <dd>

A palavra de ordem baixa desse parâmetro contém a ID do comando. A palavra de ordem alta contém o número de caracteres no buffer *pszText.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que contém o texto da ajuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
