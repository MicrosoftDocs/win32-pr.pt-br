---
description: Define o tamanho e a posição da tela de um AppBar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Mensagem de ABM_SETPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501447"
---
# <a name="abm_setpos-message"></a>\_Mensagem ABM SETPOS

Define o tamanho e a posição da tela de um AppBar. A mensagem Especifica uma borda de tela e o retângulo delimitador para o AppBar. O sistema pode ajustar o retângulo delimitador para que o AppBar não interfira na barra de tarefas do Windows nem em qualquer outro appbars.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador. Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado. Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o sistema envie a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) para todos os appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




