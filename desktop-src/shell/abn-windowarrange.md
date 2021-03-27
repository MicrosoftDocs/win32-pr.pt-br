---
description: Notifica um AppBar que o usuário selecionou o comando Cascade, Tile horizontalmente ou Tile verticalmente no lado do menu de atalho da barra de tarefas.
title: Mensagem de ABN_WINDOWARRANGE (shellapi. h)
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
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501445"
---
# <a name="abn_windowarrange-message"></a>\_Mensagem WINDOWARRANGE do ABN

Notifica um AppBar que o usuário selecionou o comando Cascade, Tile horizontalmente ou Tile verticalmente no lado do menu de atalho da barra de tarefas.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fBeginning* 
</dt> <dd>

Um sinalizador que especifica se a operação em cascata ou de bloco está começando. Esse parâmetro será **true** se a operação estiver começando e as janelas ainda não tiverem sido movidas. Será **false** se a operação tiver sido concluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O sistema envia essa mensagem de notificação duas vezes primeiro com *lParam* definido como **true** e, em seguida, com *lParam* definido como **false**. A primeira notificação é enviada antes que as janelas sejam colocadas em cascata ou em blocos postais, e a segunda é enviada depois que a operação em cascata ou bloco ocorreu.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




