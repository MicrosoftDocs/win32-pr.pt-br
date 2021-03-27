---
description: Notifica um AppBar quando um aplicativo de tela inteira está abrindo ou fechando. Essa notificação é enviada na forma de uma mensagem definida pelo aplicativo que é definida pela \_ nova mensagem ABM.
title: Mensagem de ABN_FULLSCREENAPP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090034"
---
# <a name="abn_fullscreenapp-message"></a>\_Mensagem FULLSCREENAPP do ABN

Notifica um AppBar quando um aplicativo de tela inteira está abrindo ou fechando. Essa notificação é enviada na forma de uma mensagem definida pelo aplicativo que é definida pela nova mensagem [**ABM \_**](abm-new.md) .


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fOpen* 
</dt> <dd>

Um sinalizador que especifica se um aplicativo de tela inteira está abrindo ou fechando. Esse parâmetro será **true** se o aplicativo estiver sendo aberto ou **false** se estiver fechando.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando um aplicativo de tela inteira está abrindo, um AppBar deve ser solto na parte inferior da ordem z. Quando estiver fechando, o AppBar deverá restaurar sua posição de ordem z.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




