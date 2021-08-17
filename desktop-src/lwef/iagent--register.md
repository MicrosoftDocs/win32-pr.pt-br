---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962666"
---
# <a name="iagentregister"></a>IAgent:: Register

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




