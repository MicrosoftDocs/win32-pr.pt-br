---
title: Automático
description: Determina se o depurador é iniciado automaticamente quando uma notificação RPC COM é enviada.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764455"
---
# <a name="auto"></a>Automático

Determina se o depurador é iniciado automaticamente quando uma notificação RPC COM é enviada.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ Word** .



| Valor | Descrição                    |
|-------|--------------------------------|
| 1     | Inicie o depurador automaticamente. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ DBG \_ All**](orpc-dbg-all.md)
</dt> </dl>

 

 




