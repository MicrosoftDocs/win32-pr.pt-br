---
description: Criando objetos de linha do tempo
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Criando objetos de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755993"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="e6dd1-103">Criando objetos de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="e6dd1-103">Creating Timeline Objects</span></span>

<span data-ttu-id="e6dd1-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="e6dd1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e6dd1-105">O código de exemplo apresentado neste artigo começa com uma linha do tempo vazia, mas as mesmas etapas se aplicam se você carregar um projeto existente e quiser adicionar objetos a ele.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="e6dd1-106">Para criar qualquer tipo de objeto na linha do tempo, chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="e6dd1-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="e6dd1-107">Por exemplo, o código a seguir cria um novo grupo:</span><span class="sxs-lookup"><span data-stu-id="e6dd1-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="e6dd1-108">O segundo parâmetro é um membro da enumeração [**de \_ \_ tipo principal da linha do tempo**](timeline-major-type.md) .</span><span class="sxs-lookup"><span data-stu-id="e6dd1-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="e6dd1-109">Especifica o tipo de objeto de linha do tempo a ser criado, como um grupo ou uma faixa.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="e6dd1-110">O método **CreateEmptyNode** cria o objeto e retorna um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="e6dd1-111">Ele também incrementa a contagem de referência na interface **IAMTimelineObj** , portanto, você deve liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="e6dd1-112">Não chame a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="e6dd1-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="e6dd1-113">Em vez disso, sempre use **CreateEmptyNode** para criar um objeto de linha do tempo, porque ele inicializa o novo objeto para uso em uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="e6dd1-114">A interface [**IAMTimelineObj**](iamtimelineobj.md) é uma interface genérica.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="e6dd1-115">Ele fornece métodos que são comuns a todos os tipos de objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="e6dd1-116">Cada tipo de objeto também expõe outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="e6dd1-117">Por exemplo, os grupos expõem a interface [**IAMTimelineGroup**](iamtimelinegroup.md) , entre outros.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="e6dd1-118">Você pode obter ponteiros para as outras interfaces chamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="e6dd1-119">Depois de criar um objeto, ele ainda não faz parte da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="e6dd1-120">O método para adicionar um objeto à linha do tempo depende do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="e6dd1-121">A seção a seguir descreve como adicionar grupos, composições e faixas à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="e6dd1-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6dd1-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6dd1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6dd1-123">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="e6dd1-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
