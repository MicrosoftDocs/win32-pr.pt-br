---
description: 'Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda para itens de menu ou botões da barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662602"
---
# <a name="sfvm_gethelptext-message"></a>\_Mensagem SFVM GEThelptext

Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda para itens de menu ou botões da barra de ferramentas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd \_ cchMax* \[\]
</dt> <dd>

A palavra de ordem inferior desse parâmetro contém a ID de comando. A palavra de ordem superior contém o número de caracteres no buffer *pszText* .

</dd> <dt>

*pszText* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que contém o texto de ajuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
