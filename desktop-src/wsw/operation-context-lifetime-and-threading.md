---
title: Tempo de vida do contexto de operação e threading
description: O tempo de vida do contexto de operação, representado por um \_ identificador de contexto de operação WS \_ , determina o tempo de vida das propriedades que ele contém.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Tempo de vida de contexto de operação e serviços Web de threading para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642994"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="681ac-106">Tempo de vida do contexto de operação e threading</span><span class="sxs-lookup"><span data-stu-id="681ac-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="681ac-107">O tempo de vida do contexto de operação, representado por um identificador de [ \_ \_ contexto de operação WS](ws-operation-context.md) , determina o tempo de vida das propriedades que ele contém.</span><span class="sxs-lookup"><span data-stu-id="681ac-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="681ac-108">Portanto, um contexto só deve ser usado dentro do tempo de vida da [operação de serviço](service-operation.md) ou do retorno de chamada para o qual ele foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="681ac-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="681ac-109">O tempo de vida de uma chamada síncrona é a execução da própria função.</span><span class="sxs-lookup"><span data-stu-id="681ac-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="681ac-110">Para uma chamada assíncrona, o tempo de vida termina quando a chamada assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="681ac-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="681ac-111">O modelo de serviço não fornece nenhuma garantia sobre o contexto quando a chamada é concluída.</span><span class="sxs-lookup"><span data-stu-id="681ac-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="681ac-112">O comportamento de depender do contexto de operação ou de qualquer uma de suas propriedades além de seu tempo de vida é indefinido.</span><span class="sxs-lookup"><span data-stu-id="681ac-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="681ac-113">Consulte também o exemplo de calculadora baseado em sessão, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="681ac-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="681ac-114">Modelo de threading</span><span class="sxs-lookup"><span data-stu-id="681ac-114">Threading Model</span></span>

<span data-ttu-id="681ac-115">O contexto de operação dá suporte a threads livres, mas isso é verdadeiro no próprio contexto de operação e não se aplica a nenhuma das propriedades que ele contém.</span><span class="sxs-lookup"><span data-stu-id="681ac-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="681ac-116">Ao registrar um retorno de chamada de cancelamento para uma operação de serviço por meio da função [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , observe que o primeiro registro terá sucesso; a definição do retorno de chamada de cancelamento várias vezes, no entanto, falhará.</span><span class="sxs-lookup"><span data-stu-id="681ac-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




