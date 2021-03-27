---
description: Notifica um AppBar que o estado de ocultar automaticamente ou sempre visível da barra de tarefas foi alterado&\# 8212; ou seja, o usuário selecionou ou limpou o &\# 0034; Sempre no início&\# 0034; ou &\# 0034; Caixa de seleção Ocultar automaticamente&\# 0034; na folha de propriedades da barra de tarefas.
title: Mensagem de ABN_STATECHANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826897"
---
# <a name="abn_statechange-message"></a>\_Mensagem STATECHANGE do ABN

Notifica um AppBar que o estado de ocultar automaticamente ou sempre visível da barra de tarefas foi alterado ou seja, o usuário selecionou ou desmarcou a caixa de seleção "sempre visível" ou "ocultar automaticamente" na folha de propriedades da barra de tarefas.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um AppBar pode usar essa mensagem de notificação para definir seu estado de acordo com a barra de tarefas, se desejado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




