---
description: Atualiza um objeto passando um ponteiro para uma matriz de dois ponteiros para listas de identificadores de item (PIDLs). Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_UPDATEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172069"
---
# <a name="sfvm_updateobject-message"></a>\_Mensagem SFVM UpdateObject

Atualiza um objeto passando um ponteiro para uma matriz de dois ponteiros para listas de identificadores de item (PIDLs). Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppidl* \[ no\]
</dt> <dd>

O endereço de uma matriz de dois PIDLs. O primeiro PIDL é o antigo PIDL. A segunda é uma cópia do antigo PIDL com informações atualizadas. O controle sobre o tempo de vida da cópia pertence ao modo de exibição após a conclusão bem-sucedida desta chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a ID de ListView do objeto atualizado se a atualização foi bem-sucedida; caso contrário, retornará-1.

## <a name="remarks"></a>Comentários

Se a atualização não tiver sido bem-sucedida, o chamador deverá liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




