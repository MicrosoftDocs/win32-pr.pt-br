---
description: Erros de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Erros de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811570"
---
# <a name="client-side-errors"></a><span data-ttu-id="60fd8-103">Erros de Client-Side</span><span class="sxs-lookup"><span data-stu-id="60fd8-103">Client-Side Errors</span></span>

<span data-ttu-id="60fd8-104">As falhas do lado do cliente são tratadas de forma semelhante às falhas do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="60fd8-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="60fd8-105">O [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pode mover uma mensagem para sua fila de destino se, por exemplo, a mensagem não puder ser movida do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="60fd8-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="60fd8-106">Nesse caso, a mensagem é movida para a fila de mensagens mortas do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="60fd8-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="60fd8-107">O serviço de componentes em fila COM+ monitora a fila de mensagens mortas.</span><span class="sxs-lookup"><span data-stu-id="60fd8-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="60fd8-108">Se as mensagens tiverem sido movidas, o serviço de componentes em fila criará uma instância da classe de exceção e chamará [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span><span class="sxs-lookup"><span data-stu-id="60fd8-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="60fd8-109">Se isso for bem-sucedido, o monitor da fila de mensagens mortas invocará [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span><span class="sxs-lookup"><span data-stu-id="60fd8-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="60fd8-110">O objeto pode tomar alguma atitude para reverter o efeito de uma transação anterior.</span><span class="sxs-lookup"><span data-stu-id="60fd8-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="60fd8-111">Se a reprodução for confirmada, a mensagem será removida da fila de mensagens mortas da transação.</span><span class="sxs-lookup"><span data-stu-id="60fd8-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="60fd8-112">Se a reprodução falhar ou se o CLSID e a interface necessários não estiverem disponíveis, a mensagem permanecerá na fila de mensagens mortas do transação.</span><span class="sxs-lookup"><span data-stu-id="60fd8-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="60fd8-113">Se você precisar intervir no processo descrito acima ou se precisar mover uma mensagem suspeita para fora de sua fila de repouso final, use o utilitário de movimentação de mensagem.</span><span class="sxs-lookup"><span data-stu-id="60fd8-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="60fd8-114">Para obter mais informações sobre o utilitário de movimentação de mensagens, consulte [tratamento de erros](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="60fd8-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60fd8-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60fd8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60fd8-116">Falhas de Client-Side persistentes</span><span class="sxs-lookup"><span data-stu-id="60fd8-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="60fd8-117">Erros do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="60fd8-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
