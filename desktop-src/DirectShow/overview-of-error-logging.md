---
description: Visão geral do log de erros
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Visão geral do log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087555"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="14d75-103">Visão geral do log de erros</span><span class="sxs-lookup"><span data-stu-id="14d75-103">Overview of Error Logging</span></span>

<span data-ttu-id="14d75-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="14d75-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="14d75-105">Para dar aos aplicativos flexibilidade máxima no tratamento de erros, os [serviços de edição do DirectShow](directshow-editing-services.md) usam um mecanismo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="14d75-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="14d75-106">Seu aplicativo implementa um método para registrar um erro.</span><span class="sxs-lookup"><span data-stu-id="14d75-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="14d75-107">Em tempo de execução, se ocorrer um erro, o DES chamará o método que você forneceu.</span><span class="sxs-lookup"><span data-stu-id="14d75-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="14d75-108">O método usa parâmetros que descrevem o erro.</span><span class="sxs-lookup"><span data-stu-id="14d75-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="14d75-109">O que o método faz com essas informações cabe a você.</span><span class="sxs-lookup"><span data-stu-id="14d75-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="14d75-110">(No entanto, ele deve retornar o mais rápido possível, ou pode interferir na execução do programa.)</span><span class="sxs-lookup"><span data-stu-id="14d75-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="14d75-111">O método de retorno de chamada de log de erros está contido em uma interface COM, [**IAMErrorLog**](iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="14d75-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="14d75-112">Seu aplicativo deve implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="14d75-112">Your application must implement this interface.</span></span> <span data-ttu-id="14d75-113">Como todas as interfaces COM, **IAMErrorLog** herda a interface **IUnknown** , de modo que seu aplicativo também deve implementá-la.</span><span class="sxs-lookup"><span data-stu-id="14d75-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="14d75-114">Você tem várias opções para implementar essas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="14d75-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="14d75-115">Você pode usar o Active Template Library (ATL), que fornece implementações de estoque dos métodos **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="14d75-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="14d75-116">O DirectShow também fornece uma classe base do C++, [**CUnknown**](cunknown.md), que facilita a implementação de uma interface com.</span><span class="sxs-lookup"><span data-stu-id="14d75-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="14d75-117">Para obter informações sobre como usar o **CUnknown**, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="14d75-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="14d75-118">O código de exemplo neste artigo define uma classe C++ independente, que implementa **IUnknown** e **IAMErrorLog**.</span><span class="sxs-lookup"><span data-stu-id="14d75-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="14d75-119">O resultado não é um objeto COM verdadeiro, porque ele não dá suporte a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="14d75-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="14d75-120">No entanto, essa abordagem é adequada para a finalidade do exemplo.</span><span class="sxs-lookup"><span data-stu-id="14d75-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14d75-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14d75-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14d75-122">Erros de log</span><span class="sxs-lookup"><span data-stu-id="14d75-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



