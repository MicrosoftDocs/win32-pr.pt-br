---
title: HWINEVENTHOOK (Windef.h)
description: Usado para declarar uma função de gancho de evento de janela.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a26a2593af7db4520248b5ee319fd4143a79ab1393cef02365d1fe3ea8cc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994146"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Usado para declarar uma função de gancho de evento de janela.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Comentários

Esse tipo de dados é usado com a função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e as funções [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e [**UnhookWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                          |
| Redistribuível<br/>          | Acessibilidade Ativa 1.3 RDK no Windows NT 4.0 com SP6 e posterior e Windows 95<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Windef.h (WINVER >= 0x0500) (incluir Windows.h)</dt> </dl> |



 

 





