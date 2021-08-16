---
description: Recupera os estados autohide e always on-top da barra de Windows tarefas.
title: ABM_GETSTATE mensagem (Shellapi.h)
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
ms.openlocfilehash: b1a3618be793f4728dc6184b50b7a4e0e57c3ffd2c4d2cd8acde17372aa031f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225225"
---
# <a name="abm_getstate-message"></a>Mensagem \_ GETSTATE do ABM

Recupera os estados autohide e always on-top da barra de Windows tarefas.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Ponteiro para uma [**estrutura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Você deve especificar o **membro cbSize** ao enviar essa mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se a barra de tarefas não estiver no estado autohide nem always on-top. Caso contrário, o valor de retorno será um ou ambos os seguintes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>A barra de tarefas está no estado always on-top. <br/>
<blockquote>
[!Note]<br />
A partir Windows 7, ABS_ALWAYSONTOP é retornado porque a barra de tarefas está sempre nesse estado. O código mais antigo deve ser atualizado para ignorar a ausência desse valor, não pressupondo que o valor de retorno significa que a barra de tarefas não está no estado always on-top.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>A barra de tarefas está no estado de autohide.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




