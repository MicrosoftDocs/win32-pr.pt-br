---
title: Dicas de desempenho de RPC diversas
description: Esta seção aborda diversas dicas de desempenho para o desenvolvimento de servidores RPC de alto desempenho. Esta seção fornece muitas dicas que se referem ao cliente RPC. Desenvolver um cliente RPC corretamente permite que o servidor RPC execute menos trabalho.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005151"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="f8e7b-105">Dicas de desempenho de RPC diversas</span><span class="sxs-lookup"><span data-stu-id="f8e7b-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="f8e7b-106">Esta seção aborda diversas dicas de desempenho para o desenvolvimento de servidores RPC de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="f8e7b-107">Esta seção fornece muitas dicas que se referem ao cliente RPC.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="f8e7b-108">Desenvolver um cliente RPC corretamente permite que o servidor RPC execute menos trabalho.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="f8e7b-109">Usar Kerberos</span><span class="sxs-lookup"><span data-stu-id="f8e7b-109">Use Kerberos</span></span>

<span data-ttu-id="f8e7b-110">Se a segurança for usada, use o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="f8e7b-111">No lado do servidor, o Kerberos não requer acesso ao KDC.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="f8e7b-112">Isso move a carga de trabalho do servidor para o cliente, que fornece servidores de melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="f8e7b-113">Usar o rastreamento de identidade estático</span><span class="sxs-lookup"><span data-stu-id="f8e7b-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="f8e7b-114">Se a segurança for usada, tente usar o rastreamento de identidade estático.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="f8e7b-115">O rastreamento de identidade estático é mais barato em termos de uso de recursos do que o controle de identidade dinâmico.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="f8e7b-116">Se a identidade do cliente for alterada e o servidor não estiver ciente da alteração, use o controle dinâmico em vez de criar um identificador de associação diferente para cada identidade.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="f8e7b-117">Mas se a identidade for a mesma, verifique se a RPC está ciente desse fato para evitar que o RPC faça verificações de identidades alteradas a cada vez.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="f8e7b-118">Usar a função RpcGetAuthorizationContextForClient</span><span class="sxs-lookup"><span data-stu-id="f8e7b-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="f8e7b-119">Se você precisar verificar o acesso no Windows XP, use a função [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="f8e7b-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="f8e7b-120">Os contextos de Authz resultantes permitem verificações de acesso muito rápidas, que são armazenadas em cache de forma eficiente pelo tempo de execução de RPC.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="f8e7b-121">Não modifique o token, a menos que seja necessário</span><span class="sxs-lookup"><span data-stu-id="f8e7b-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="f8e7b-122">Se o controle de identidade dinâmico for usado, não modifique o token de thread/processo, a menos que seja absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="f8e7b-123">Mesmo que ele seja modificado para as configurações que tinha anteriormente, o token geralmente é suficientemente diferente para o sistema de segurança disparar o estabelecimento de um novo contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="f8e7b-124">Considere a serialização de modo misto para identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="f8e7b-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="f8e7b-125">O modo de serialização padrão para o identificador de contexto é serializado (exclusivo).</span><span class="sxs-lookup"><span data-stu-id="f8e7b-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="f8e7b-126">Considere fazer todas as chamadas que não modificam o estado do identificador de contexto no modo de serialização compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="f8e7b-127">Consulte [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f8e7b-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




