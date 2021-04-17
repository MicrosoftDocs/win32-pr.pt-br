---
title: Sincronização de retorno de chamada
description: Sincronização de retorno de chamada
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105798450"
---
# <a name="callback-synchronization"></a><span data-ttu-id="79ce1-103">Sincronização de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="79ce1-103">Callback Synchronization</span></span>

<span data-ttu-id="79ce1-104">A [API do Wininet](/windows/desktop/WinInet/portal) assíncrona (usada para os protocolos mais comuns) deixa a sincronização do mecanismo de retorno de chamada e o aplicativo de chamada como um exercício para o cliente.</span><span class="sxs-lookup"><span data-stu-id="79ce1-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="79ce1-105">Isso é intencional porque permite o maior grau de flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="79ce1-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="79ce1-106">Os protocolos padrão e a implementação do moniker da URL executam essa sincronização e garantem que aplicativos de thread único e apartamento não precisem lidar com a contenção no estilo de thread livre.</span><span class="sxs-lookup"><span data-stu-id="79ce1-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="79ce1-107">Ou seja, as interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) do cliente são chamadas somente em seus threads apropriados.</span><span class="sxs-lookup"><span data-stu-id="79ce1-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="79ce1-108">Esse recurso é transparente para o usuário da URL mMoniker, desde que cada thread que chama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) tenha uma fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="79ce1-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="79ce1-109">A especificação de moniker assíncrona requer um controle mais preciso sobre a priorização e o gerenciamento de downloads do que o é permitido pelo WinSock ou pelo WinInet.</span><span class="sxs-lookup"><span data-stu-id="79ce1-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="79ce1-110">Da mesma forma, um moniker de URL gerencia todos os downloads de qualquer thread do chamador específico, usando (como parte de sua sincronização) um esquema de prioridade baseado na especificação [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="79ce1-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79ce1-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79ce1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ce1-112">Identificadores de URL</span><span class="sxs-lookup"><span data-stu-id="79ce1-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 