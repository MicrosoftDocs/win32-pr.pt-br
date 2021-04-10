---
title: Anotação do servidor
description: Esta seção fornece informações sobre como usar a anotação do servidor.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005128"
---
# <a name="server-annotation"></a><span data-ttu-id="69d49-103">Anotação do servidor</span><span class="sxs-lookup"><span data-stu-id="69d49-103">Server Annotation</span></span>

<span data-ttu-id="69d49-104">Esta seção fornece informações sobre como usar a anotação do servidor.</span><span class="sxs-lookup"><span data-stu-id="69d49-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="69d49-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="69d49-105">Summary</span></span>

<span data-ttu-id="69d49-106">Você define uma classe que implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), cria uma instância dela e informa ao sistema que você deseja que ela substitua propriedades específicas em elementos específicos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="69d49-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="69d49-107">Quando um cliente solicita uma das propriedades de um dos elementos da interface do usuário, seu objeto é chamado e recebe uma oportunidade de fornecer um valor.</span><span class="sxs-lookup"><span data-stu-id="69d49-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="69d49-108">Se o objeto retornar um valor, esse valor será passado de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="69d49-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="69d49-109">Se o objeto não retornar um valor, o valor padrão desse elemento de interface do usuário será retornado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="69d49-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="69d49-110">Quando usar essa técnica</span><span class="sxs-lookup"><span data-stu-id="69d49-110">When to Use This Technique</span></span>

<span data-ttu-id="69d49-111">Use essa técnica quando desejar substituir as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um objeto.</span><span class="sxs-lookup"><span data-stu-id="69d49-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="69d49-112">Essa técnica é muito mais simples do que as técnicas de **IAccessible** anteriores.</span><span class="sxs-lookup"><span data-stu-id="69d49-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="69d49-113">Para obter mais informações, consulte [alternativas à anotação dinâmica](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="69d49-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="69d49-114">Você não pode usar a anotação de servidor para alterar a estrutura de objetos expostos.</span><span class="sxs-lookup"><span data-stu-id="69d49-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="69d49-115">Para alterar a estrutura de um objeto, você deve implementar um ponteiro de interface de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.</span><span class="sxs-lookup"><span data-stu-id="69d49-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="69d49-116">Para obter mais informações sobre a anotação do servidor, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="69d49-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="69d49-117">Usando a anotação do servidor</span><span class="sxs-lookup"><span data-stu-id="69d49-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="69d49-118">Exemplo de anotação do servidor</span><span class="sxs-lookup"><span data-stu-id="69d49-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




