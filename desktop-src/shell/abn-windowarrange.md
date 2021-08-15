---
description: Notifica uma barra de aplicativos de que o usuário selecionou o comando Cascade, Lado a Lado Horizontalmente ou Lado Verticalmente no menu de atalho da barra de tarefas.
title: ABN_WINDOWARRANGE mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225017"
---
# <a name="abn_windowarrange-message"></a>Mensagem \_ WINDOWARRANGE do ABN

Notifica uma barra de aplicativos de que o usuário selecionou o comando Cascade, Lado a Lado Horizontalmente ou Lado Verticalmente no menu de atalho da barra de tarefas.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fBeginning* 
</dt> <dd>

Um sinalizador que especifica se a operação em cascata ou de um tile está começando. Esse parâmetro será **TRUE** se a operação estiver começando e as janelas ainda não foram movidas. Será **FALSE se** a operação tiver sido concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O sistema envia essa mensagem de notificação duas vezes primeiro *com lParam definido* como **TRUE** e, em seguida, com *lParam definido* como **FALSE.** A primeira notificação é enviada antes que as janelas sejam em cascata ou lado a lado e a segunda é enviada após a operação em cascata ou de bloco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




