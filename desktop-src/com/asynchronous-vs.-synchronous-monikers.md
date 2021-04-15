---
title: Monikers assíncronos e síncronos
description: Monikers assíncronos e síncronos
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104561676"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Monikers assíncronos e síncronos

Um cliente de um moniker OLE síncrono padrão normalmente cria e mantém uma referência ao moniker, bem como o contexto de associação a ser usado durante a associação. Os componentes envolvidos no uso de monikers tradicionais são mostrados no diagrama a seguir.

![Diagrama que mostra o cliente conectado a um contexto de associação ou qualquer moniker para o fornecido pelo sistema.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Os clientes normalmente criam monikers padrão chamando funções como [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)ou [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) ou, pois eles podem ser salvos no armazenamento persistente, por meio de [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) e [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). Os monikers também podem ser obtidos de um objeto de contêiner chamando o método [**IBindHost:: createmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) . Os clientes criam contextos de ligação chamando a função [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) e, em seguida, passam o contexto de associação para o moniker com chamadas para [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Conforme mostrado no diagrama a seguir, um cliente de um moniker assíncrono também cria e mantém uma referência ao moniker e ao contexto de associação a ser usado durante a associação.

![Diagrama que mostra as conexões entre o cliente, fornecido pelo Monker e fornecido pelo sistema.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Para obter o comportamento assíncrono, o cliente implementa a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) em um objeto BIND-status-retorno de chamada e chama a função [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) ou a função [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) para registrar essa interface com o contexto de associação. O moniker passa um ponteiro para sua interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) em uma chamada para o método [**IBindStatusCallback:: OnStart**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) . O cliente informa ao moniker assíncrono como ele deseja associar ao retorno da chamada do moniker ao método [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 