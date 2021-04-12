---
title: Armazenamento assíncrono e síncrono
description: Armazenamento assíncrono e síncrono
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499168"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="6df09-103">Armazenamento assíncrono e síncrono</span><span class="sxs-lookup"><span data-stu-id="6df09-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="6df09-104">Os monikers assíncronos também podem retornar um objeto de [armazenamento assíncrono](/windows/desktop/Stg/asynchronous-storage) na notificação [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6df09-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="6df09-105">Esse objeto de armazenamento pode permitir o acesso a alguns dos dados persistentes do objeto enquanto a associação ainda está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6df09-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="6df09-106">Um cliente pode escolher entre dois modos para o armazenamento: bloqueio e não bloqueio.</span><span class="sxs-lookup"><span data-stu-id="6df09-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="6df09-107">No modo de bloqueio, que é compatível com as implementações atuais de objetos de armazenamento, se os dados estiverem indisponíveis, a chamada será bloqueada até que os dados cheguem.</span><span class="sxs-lookup"><span data-stu-id="6df09-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="6df09-108">No modo de não bloqueio, em vez de bloquear a chamada, o objeto de armazenamento retorna um novo erro E \_ pendente quando os dados não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6df09-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="6df09-109">Um cliente que reconhece a associação assíncrona e o armazenamento observa esse erro e aguarda outras notificações ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para repetir a operação.</span><span class="sxs-lookup"><span data-stu-id="6df09-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="6df09-110">Um cliente pode escolher entre um armazenamento síncrono (bloqueio) e assíncrono (não bloqueado) escolhendo se deseja definir o \_ sinalizador BINDF ASYNCSTORAGE no valor *grfBINDF* retornado para [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6df09-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df09-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6df09-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df09-112">Monikers assíncronos</span><span class="sxs-lookup"><span data-stu-id="6df09-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 