---
description: Define os Estados de ocultar automaticamente e sempre visível da barra de tarefas do Windows.
title: Mensagem de ABM_SETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967373"
---
# <a name="abm_setstate-message"></a>\_Mensagem ABM SETstate

Define os Estados de ocultar automaticamente e sempre visível da barra de tarefas do Windows.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem. Os dados para o estado desejado são enviados no membro **lParam** usando um dos valores a seguir.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Ocultar automaticamente e sempre ativo-superior

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ALWAYSONTOP de ABS \_**


</dt> <dd>

Sempre visível, ocultar automaticamente

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**AutoOcultar do ABS \_**


</dt> <dd>

Ocultar automaticamente, sempre visível

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ ocultar \| ABS \_ ALWAYSONTOP**


</dt> <dd>

Ocultar automaticamente e sempre em cima

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




