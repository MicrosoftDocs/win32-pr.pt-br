---
title: Depuração (serviços Web do Windows)
description: Um conjunto de funções só está disponível na compilação de depuração e destina-se a testes e depuração.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depuração de serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105788705"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="ceee1-106">Depuração (serviços Web do Windows)</span><span class="sxs-lookup"><span data-stu-id="ceee1-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="ceee1-107">Um conjunto de funções só está disponível na compilação de depuração e destina-se a testes e depuração.</span><span class="sxs-lookup"><span data-stu-id="ceee1-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="ceee1-108">Há várias funções e variáveis de ambiente disponíveis somente no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="ceee1-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="ceee1-109">Eles podem ser usados para ajudar no teste e na depuração.</span><span class="sxs-lookup"><span data-stu-id="ceee1-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="ceee1-110">A configuração de WsTimeout = 0 fará com que todos os tempos limite sejam INFINITOs.</span><span class="sxs-lookup"><span data-stu-id="ceee1-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="ceee1-111">Isso é útil ao percorrer o depurador durante operações sensíveis ao tempo.</span><span class="sxs-lookup"><span data-stu-id="ceee1-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="ceee1-112">A definição de WsFailCount tem o mesmo efeito que chamar WsSetAutoFail.</span><span class="sxs-lookup"><span data-stu-id="ceee1-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="ceee1-113">WsFlags permite que você defina vários sinalizadores que modificam o comportamento de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ceee1-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="ceee1-114">A sintaxe é WsFlags = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="ceee1-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="ceee1-115">Os sinalizadores com suporte são ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest e ModifySignatureValue.</span><span class="sxs-lookup"><span data-stu-id="ceee1-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="ceee1-116">As funções a seguir são usadas com a depuração:</span><span class="sxs-lookup"><span data-stu-id="ceee1-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="ceee1-117">**WsDumpMemory**</span><span class="sxs-lookup"><span data-stu-id="ceee1-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="ceee1-118">**WsSetAutoFail**</span><span class="sxs-lookup"><span data-stu-id="ceee1-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




