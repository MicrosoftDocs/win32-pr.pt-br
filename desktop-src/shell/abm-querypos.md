---
description: Solicita um tamanho e uma posição de tela para um AppBar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Mensagem de ABM_QUERYPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296222"
---
# <a name="abm_querypos-message"></a>\_Mensagem ABM QUERYPOS

Solicita um tamanho e uma posição de tela para um AppBar. Quando a solicitação é feita, a mensagem propõe uma borda de tela e um retângulo delimitador para o AppBar. O sistema ajusta o retângulo delimitador para que o AppBar não interfira na barra de tarefas do Windows ou em qualquer outro appbars.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador proposto. Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado. Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Um AppBar deve enviar essa mensagem antes de enviar a mensagem [**\_ SETPOS do ABM**](abm-setpos.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




