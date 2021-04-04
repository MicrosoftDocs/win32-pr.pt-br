---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822680"
---
# <a name="iagentregister"></a>IAgent:: Register

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registra um coletor de notificação para o aplicativo cliente.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Endereço de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) para sua interface de coletor de notificação.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Endereço da ID do coletor de notificação (usado para cancelar o registro do coletor de notificação).

</dd> </dl>

Você precisa registrar seu coletor de notificações (também conhecido como coletor de notificação ou coletor de eventos) para receber eventos do servidor do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgent:: cancelar registro**](iagent--unregister.md)


 

 




