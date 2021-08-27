---
description: recupera os estados de autoocultar e sempre visível da barra de tarefas Windows.
title: Mensagem de ABM_GETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466383"
---
# <a name="abm_getstate-message"></a>\_Mensagem GETstate do ABM

recupera os estados de autoocultar e sempre visível da barra de tarefas Windows.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Você deve especificar o membro **cbSize** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se a barra de tarefas não estiver no estado de ocultar automaticamente ou sempre visível. Caso contrário, o valor de retorno será um ou ambos os seguintes:




| Código de retorno | Descrição | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | A barra de tarefas está no estado sempre visível. <br /><blockquote>[!Note]<br />a partir do Windows 7, ABS_ALWAYSONTOP não é mais retornado porque a barra de tarefas sempre está nesse estado. O código mais antigo deve ser atualizado para ignorar a ausência desse valor em não pressupor que o valor de retorno signifique que a barra de tarefas não está no estado sempre visível.</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | A barra de tarefas está no estado de AutoOcultar.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




