---
description: A parte mais problemática de escrever componentes é lidar com possíveis erros.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Tratamento de erros no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089693"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="c2581-103">Tratamento de erros no COM+</span><span class="sxs-lookup"><span data-stu-id="c2581-103">Handling Errors in COM+</span></span>

<span data-ttu-id="c2581-104">A parte mais problemática de escrever componentes é lidar com possíveis erros.</span><span class="sxs-lookup"><span data-stu-id="c2581-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="c2581-105">Tentar determinar o que pode dar errado e o que fazer sobre ele pode ser desafiador nas melhores condições.</span><span class="sxs-lookup"><span data-stu-id="c2581-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="c2581-106">Erros comuns que seu componente pode verificar e identificadores são conexões de rede com falha, erros de segurança e falhas associadas a objetos inacessíveis.</span><span class="sxs-lookup"><span data-stu-id="c2581-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="c2581-107">Além disso, você pode desenvolver seus próprios códigos de erro para relatar erros específicos da interface, como quando uma regra de negócios foi violada.</span><span class="sxs-lookup"><span data-stu-id="c2581-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="c2581-108">Ao manter o modelo de programação COM+, um objeto pode (e geralmente faz) chamar métodos de interface em outros objetos para executar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2581-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="c2581-109">Como os programadores podem escrever componentes em linguagens de programação diferentes, o COM+ requer que todos os mecanismos de tratamento de erros sejam neutros à linguagem, por exemplo: HRESULTs e coleções [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c2581-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="c2581-110">Esta seção inclui tópicos, descritos na tabela a seguir, que discutem técnicas para lidar com erros em aplicativos COM+, recursos no COM+ que afetam o comportamento de falha e sugestões para diagnosticar erros COM+.</span><span class="sxs-lookup"><span data-stu-id="c2581-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="c2581-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="c2581-111">Topic</span></span>                                                                                           | <span data-ttu-id="c2581-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2581-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2581-113">Estratégias para lidar com erros no COM+</span><span class="sxs-lookup"><span data-stu-id="c2581-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="c2581-114">Lista e descreve as diretrizes básicas para lidar com erros no COM+, incluindo quando usar as coleções HRESULTs e [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c2581-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="c2581-115">Como o COM+ modifica valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c2581-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="c2581-116">Identifica a única condição na qual o COM+ converte um HRESULT padrão em um código de erro COM+ antes de passá-lo de volta para o chamador.</span><span class="sxs-lookup"><span data-stu-id="c2581-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="c2581-117">Política de FailFast e isolamento de falhas</span><span class="sxs-lookup"><span data-stu-id="c2581-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="c2581-118">Mostra como o isolamento de falhas e a política de FailFast afetam o comportamento do COM+.</span><span class="sxs-lookup"><span data-stu-id="c2581-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="c2581-119">Localizando a origem de um erro</span><span class="sxs-lookup"><span data-stu-id="c2581-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="c2581-120">Descreve como você pode diagnosticar a origem e obter uma descrição dos erros do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2581-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="c2581-121">Interpretando códigos de erro</span><span class="sxs-lookup"><span data-stu-id="c2581-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="c2581-122">Identifica o mecanismo predominante de tratamento de erros para Microsoft Visual C++, a linguagem Java e o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c2581-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="c2581-123">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="c2581-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="c2581-124">Fornece assistência adicional no diagnóstico de erros.</span><span class="sxs-lookup"><span data-stu-id="c2581-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c2581-125">Entrando em contato com o suporte</span><span class="sxs-lookup"><span data-stu-id="c2581-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="c2581-126">Identifica informações importantes de solução de problemas que você deve fornecer ao contatar o suporte.</span><span class="sxs-lookup"><span data-stu-id="c2581-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="c2581-127">Para obter informações detalhadas sobre como lidar com erros associados a vários serviços COM+, consulte as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="c2581-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="c2581-128">Acelerando as transações notificando o objeto raiz</span><span class="sxs-lookup"><span data-stu-id="c2581-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="c2581-129">[Tratamento de erros](handling-errors-in-queued-components.md) (para componentes na fila)</span><span class="sxs-lookup"><span data-stu-id="c2581-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2581-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2581-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2581-131">Depurando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="c2581-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




