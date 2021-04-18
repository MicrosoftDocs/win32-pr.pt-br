---
description: Política de FailFast e isolamento de falhas
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Política de FailFast e isolamento de falhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500895"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="e0b3c-103">Política de FailFast e isolamento de falhas</span><span class="sxs-lookup"><span data-stu-id="e0b3c-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="e0b3c-104">O COM+ executa amplas verificações de consistência e integridade interna.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="e0b3c-105">Se o COM+ encontrar uma condição de erro interno inesperada, ele encerrará imediatamente o processo.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="e0b3c-106">Essa política, chamada *FailFast*, facilita a contenção de falhas e resulta em sistemas mais confiáveis e robustos.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="e0b3c-107">Considere um caso em que o COM+ detecta que uma de suas estruturas de dados está em um estado corrompido.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="e0b3c-108">Neste ponto, a causa e a magnitude da corrupção são desconhecidas e, infelizmente, o COM+ não pode dizer até que distância o dano se espalha.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="e0b3c-109">No entanto, embora o COM+ esteja em um estado indeterminado, ele não é executado isoladamente.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="e0b3c-110">Assim como outras DLLs, ela é hospedada em um ambiente de processo e compartilha um único espaço de endereço com o executável do programa principal e muitas outras DLLs.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="e0b3c-111">Portanto, o COM+ pressupõe que todo o processo foi corrompido, e o processo é imediatamente encerrado para impedir que ele espalhe informações potencialmente corrompidas para outros processos ou, pior ainda, de permitir que os dados corrompidos sejam confirmados e tornados duráveis.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="e0b3c-112">COM+ não permite que exceções se propaguem fora de um contexto.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="e0b3c-113">Se ocorrer uma exceção durante a execução em um contexto COM+ e o aplicativo não capturar a exceção antes de retornar do contexto, o COM+ capturará a exceção e encerrará o processo.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="e0b3c-114">Usar a política FailFast nesse caso se baseia na suposição de que a exceção colocou o processo em um estado indeterminado; Não é seguro continuar o processamento.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="e0b3c-115">Como desenvolvedor ou administrador, você deve inspecionar o log do aplicativo Visualizador de Eventos para obter detalhes sobre qualquer ação de FailFast ou erros graves de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0b3c-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0b3c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0b3c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b3c-117">Localizando a origem de um erro</span><span class="sxs-lookup"><span data-stu-id="e0b3c-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="e0b3c-118">Como o COM+ modifica valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e0b3c-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="e0b3c-119">Interpretando códigos de erro</span><span class="sxs-lookup"><span data-stu-id="e0b3c-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="e0b3c-120">Estratégias para lidar com erros no COM+</span><span class="sxs-lookup"><span data-stu-id="e0b3c-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="e0b3c-121">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="e0b3c-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



