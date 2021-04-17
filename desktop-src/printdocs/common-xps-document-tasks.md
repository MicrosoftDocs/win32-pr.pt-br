---
description: Esta página lista algumas das tarefas de programação que normalmente são executadas com a API de documento XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tarefas comuns de programação de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775577"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="a7f46-103">Tarefas comuns de programação de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="a7f46-104">Esta página lista algumas das tarefas de programação que normalmente são executadas com a API de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="a7f46-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="a7f46-105">Tarefas comuns do documento XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="a7f46-106">Os exemplos de código a seguir ilustram algumas das tarefas de programação que normalmente são executadas quando a API de documento XPS é usada para trabalhar com um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="a7f46-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="a7f46-107">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="a7f46-108">Criar um OM XPS em branco</span><span class="sxs-lookup"><span data-stu-id="a7f46-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="a7f46-109">Ler um documento XPS em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="a7f46-110">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="a7f46-111">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="a7f46-112">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="a7f46-113">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="a7f46-114">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="a7f46-115">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="a7f46-116">Trabalhando com interfaces de coleção de OM XPS</span><span class="sxs-lookup"><span data-stu-id="a7f46-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="a7f46-117">Isenção de responsabilidade</span><span class="sxs-lookup"><span data-stu-id="a7f46-117">Disclaimer</span></span>

<span data-ttu-id="a7f46-118">Os exemplos de código não se destinam a serem programas completos e em funcionamento.</span><span class="sxs-lookup"><span data-stu-id="a7f46-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="a7f46-119">Os exemplos de código que são referenciados nesta página, por exemplo, não executam verificação de parâmetros, verificação de erros ou tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="a7f46-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="a7f46-120">Use esses exemplos como ponto de partida e, em seguida, adicione o código necessário para criar um aplicativo robusto.</span><span class="sxs-lookup"><span data-stu-id="a7f46-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="a7f46-121">Para obter mais informações sobre valores de retorno **HRESULT** e estratégias de tratamento de erros, consulte [tratamento de erros em com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="a7f46-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="a7f46-122">Antes que as interfaces do XPS OM possam ser usadas, o COM deve ser inicializado no thread, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7f46-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="a7f46-123">Para maior clareza, esses exemplos de código usam um OM XPS muito simples, um que pode não ser complexo o suficiente para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f46-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="a7f46-124">Como um caso no ponto, nos exemplos de código que adicionam conteúdo a uma página, os elementos visuais de uma página são adicionados diretamente à lista de objetos visuais da página; no entanto, na prática, você pode querer agrupar objetos visuais em objetos Canvas, para que vários objetos possam ser afetados como um grupo.</span><span class="sxs-lookup"><span data-stu-id="a7f46-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="a7f46-125">Portanto, para habilitar o suporte do mesmo conteúdo para mais de um tamanho de página, você pode agrupar o conteúdo visual de uma página em um único objeto Canvas e, em seguida, aplicar uma transformação à tela para dimensioná-la para o tamanho da página atual.</span><span class="sxs-lookup"><span data-stu-id="a7f46-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7f46-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7f46-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f46-127">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="a7f46-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="a7f46-128">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="a7f46-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
