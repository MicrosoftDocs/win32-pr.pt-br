---
title: Monikers assíncronos e síncronos
description: Monikers assíncronos e síncronos
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c631c669d73796d1596f52ab2ec6e724829ea80e6873523c1e9bd4f8ad567f09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071096"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Monikers assíncronos e síncronos

Um cliente de um moniker OLE padrão e síncrono normalmente cria e mantém uma referência ao moniker, bem como o contexto de associação a ser usado durante a associação. Os componentes envolvidos no uso de monikers tradicionais são mostrados no diagrama a seguir.

![Diagrama que mostra o cliente conectado ao Contexto de Vinculação ou a Qualquer Moniker para o Fornecido pelo Sistema.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Os clientes normalmente criam monikers padrão chamando funções como [**CreateFileMoniker,**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)ou [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) ou, porque podem ser salvos no armazenamento persistente, por meio de [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) e [**OleLoadFromStream.**](/windows/desktop/api/ole/nf-ole-oleloadfromstream) Monikers também podem ser obtidos de um objeto de contêiner chamando o [**método IBindHost::CreateMoniker.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) Os clientes criam contextos de ligação chamando a função [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) e, em seguida, passam o contexto de ligação para o moniker com chamadas para [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Conforme mostrado no diagrama a seguir, um cliente de um moniker assíncrono também cria e mantém uma referência ao moniker e ao contexto de associação a ser usado durante a associação.

![Diagrama que mostra as conexões entre o Fornecido pelo Cliente, o Que forneceu o E o Fornecido pelo Sistema.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Para obter um comportamento assíncrono, o cliente implementa a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) em um objeto bind-status-callback e chama a função [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) ou a [**função CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) para registrar essa interface com o contexto de ligação. O moniker passa um ponteiro para sua interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) em uma chamada para o [**método IBindStatusCallback::OnStartBinding.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) O cliente informa ao moniker assíncrono como ele deseja se vincular no retorno da chamada do moniker para o método [**IBindStatusCallback::GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 