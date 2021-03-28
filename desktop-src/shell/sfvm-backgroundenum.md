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
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989043"
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



 

 
