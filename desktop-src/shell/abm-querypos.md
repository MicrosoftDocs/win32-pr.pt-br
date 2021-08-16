---
description: Solicita um tamanho e uma posição de tela para um AppBar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Mensagem de ABM_QUERYPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225027"
---
# <a name="abm_querypos-message"></a>\_Mensagem ABM QUERYPOS

Solicita um tamanho e uma posição de tela para um AppBar. Quando a solicitação é feita, a mensagem propõe uma borda de tela e um retângulo delimitador para o AppBar. o sistema ajusta o retângulo delimitador para que o appbar não interfira na barra de tarefas Windows ou em qualquer outro appbars.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador proposto. Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado. Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Um AppBar deve enviar essa mensagem antes de enviar a mensagem [**\_ SETPOS do ABM**](abm-setpos.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




