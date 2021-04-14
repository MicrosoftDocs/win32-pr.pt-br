---
description: 'Notifica o objeto de retorno de chamada que o usuário clicou em um cabeçalho de coluna para classificar a lista de objetos no modo de exibição de pasta. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_COLUMNCLICK (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461258"
---
# <a name="sfvm_columnclick-message"></a>\_Mensagem SFVM COLUMNCLICK

Notifica o objeto de retorno de chamada que o usuário clicou em um cabeçalho de coluna para classificar a lista de objetos no modo de exibição de pasta. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IColumn* \[ no\]
</dt> <dd>

O índice da coluna que foi clicada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em resposta a essa notificação, você deve retornar S \_ OK para reorganizar a lista por conta própria. Para que a pasta do sistema exiba o objeto, reorganize a lista, retorne S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
