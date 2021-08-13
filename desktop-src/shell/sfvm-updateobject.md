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
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452834"
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

## <a name="return-value"></a>Valor retornado

Retorna a ID de ListView do objeto atualizado se a atualização foi bem-sucedida; caso contrário, retornará-1.

## <a name="remarks"></a>Comentários

Se a atualização não tiver sido bem-sucedida, o chamador deverá liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




