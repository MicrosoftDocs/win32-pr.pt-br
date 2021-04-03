---
title: Cancelando uma chamada assíncrona
description: Um cliente pode cancelar uma chamada assíncrona que está em andamento se o objeto de chamada implementa a interface ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084935"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="0ac57-103">Cancelando uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="0ac57-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="0ac57-104">Um cliente pode cancelar uma chamada assíncrona que está em andamento se o objeto de chamada implementa a interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="0ac57-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="0ac57-105">Para objetos que usam marshaling padrão, **ICancelMethodCalls** está sempre disponível para chamadas com marshaling.</span><span class="sxs-lookup"><span data-stu-id="0ac57-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="0ac57-106">Para objetos que usam marshaling personalizado ou para chamadas para objetos de servidor dentro do mesmo apartamento, essa funcionalidade estará disponível somente se o objeto de chamada implementar **ICancelMethodCalls**.</span><span class="sxs-lookup"><span data-stu-id="0ac57-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="0ac57-107">O cliente pode cancelar a chamada a qualquer momento, de quando o \_ método Begin é chamado até que o \_ método Finish retorne.</span><span class="sxs-lookup"><span data-stu-id="0ac57-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="0ac57-108">Se o cliente cancelar a chamada antes de chamar o \_ método Finish, ele deverá chamar o \_ método Finish para limpar o estado do objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ac57-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="0ac57-109">Até que o cliente tenha feito isso, qualquer chamada para qualquer \_ método Begin no objeto de chamada retornará RPC \_ E \_ Call \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="0ac57-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="0ac57-110">**Para cancelar uma chamada assíncrona**</span><span class="sxs-lookup"><span data-stu-id="0ac57-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="0ac57-111">Consulte o objeto de chamada para [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span><span class="sxs-lookup"><span data-stu-id="0ac57-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="0ac57-112">Chame [**ICancelMethodCalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)e, em seguida, chame [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar o ponteiro obtido pela chamada [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="0ac57-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="0ac57-113">Se o cliente ainda não tiver chamado o \_ método Finish, chame-o agora.</span><span class="sxs-lookup"><span data-stu-id="0ac57-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="0ac57-114">Não há nenhuma garantia de que o servidor realmente interrompeu a execução da chamada.</span><span class="sxs-lookup"><span data-stu-id="0ac57-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="0ac57-115">Se o trabalho adicional do cliente depende de algum estado de servidor que a chamada pode ou não ter mudado, o cliente deve determinar esse estado antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="0ac57-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ac57-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ac57-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ac57-117">Fazendo uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="0ac57-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 