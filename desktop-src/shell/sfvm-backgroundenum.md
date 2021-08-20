---
description: 'Permite que o objeto de retorno de chamada solicite a enumeração em um thread em segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_BACKGROUNDENUM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592736"
---
# <a name="sfvm_backgroundenum-message"></a>\_Mensagem SFVM BACKGROUNDENUM

Permite que o objeto de retorno de chamada solicite a enumeração em um thread em segundo plano. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

## <a name="remarks"></a>Comentários

Em resposta a essa notificação, retorne S \_ OK para habilitar a enumeração em segundo plano. Por padrão, o objeto de pasta do sistema exibirá a animação "lanterna" enquanto a enumeração estiver ocorrendo. Para especificar uma animação personalizada, manipule [**SFVM \_ getanimation**](sfvm-getanimation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
