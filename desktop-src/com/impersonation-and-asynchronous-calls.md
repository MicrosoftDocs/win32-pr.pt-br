---
title: Representação e chamadas assíncronas
description: Representação e chamadas assíncronas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641944"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="08955-103">Representação e chamadas assíncronas</span><span class="sxs-lookup"><span data-stu-id="08955-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="08955-104">O servidor não pode representar o cliente depois que a chamada do servidor para [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) for concluída, mesmo que o \_ método Begin ainda não tenha sido concluído.</span><span class="sxs-lookup"><span data-stu-id="08955-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="08955-105">Por exemplo, suponha que um cliente chame o \_ método Begin, o servidor processa a chamada imediatamente e o servidor chama o **sinal** para indicar que ele concluiu o processamento.</span><span class="sxs-lookup"><span data-stu-id="08955-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="08955-106">Mesmo se o trabalho continuar a ser feito no \_ método Begin, o servidor não poderá representar o cliente depois que a chamada para **Signal** for concluída.</span><span class="sxs-lookup"><span data-stu-id="08955-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="08955-107">Se o servidor representar o cliente antes de chamar [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), o token de representação não será removido do thread até que o servidor chame [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) ou até que a chamada do servidor para Begin \_ Returns, o que ocorrer primeiro.</span><span class="sxs-lookup"><span data-stu-id="08955-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08955-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08955-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08955-109">Delegação e representação</span><span class="sxs-lookup"><span data-stu-id="08955-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="08955-110">Fazendo uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="08955-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 