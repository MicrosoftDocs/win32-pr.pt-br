---
description: Recupera o retângulo delimitador da barra de tarefas do Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Mensagem de ABM_GETTASKBARPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501448"
---
# <a name="abm_gettaskbarpos-message"></a>\_Mensagem ABM GETTASKBARPOS

Recupera o retângulo delimitador da barra de tarefas do Windows.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) cujo membro **RC** recebe o retângulo delimitador, nas coordenadas da tela, da barra de tarefas. Você deve especificar o **cbSize** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Observe que isso se aplica somente à barra de tarefas do sistema. Outros objetos, especialmente barras de ferramentas fornecidas com software de terceiros, também podem estar presentes. Como resultado, parte da área de tela não coberta pela barra de tarefas do Windows pode não estar visível para o usuário. Para recuperar a área da tela não coberta pela barra de tarefas e por outras barras de aplicativo a área de trabalho disponível para seu aplicativo, use a função [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

