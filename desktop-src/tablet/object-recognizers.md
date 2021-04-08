---
description: Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconhecedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922268"
---
# <a name="object-recognizers"></a><span data-ttu-id="e5abc-103">Reconhecedores de objetos</span><span class="sxs-lookup"><span data-stu-id="e5abc-103">Object Recognizers</span></span>

<span data-ttu-id="e5abc-104">Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="e5abc-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="e5abc-105">Os reconhecedores de objetos reconhecem formas gerais, de acordo com sua finalidade.</span><span class="sxs-lookup"><span data-stu-id="e5abc-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="e5abc-106">Os reconhecedores de objetos são usados para reconhecer:</span><span class="sxs-lookup"><span data-stu-id="e5abc-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="e5abc-107">Notas musicais</span><span class="sxs-lookup"><span data-stu-id="e5abc-107">Musical notes</span></span>
-   <span data-ttu-id="e5abc-108">Formas geométricas</span><span class="sxs-lookup"><span data-stu-id="e5abc-108">Geometric shapes</span></span>
-   <span data-ttu-id="e5abc-109">Equações matemáticas</span><span class="sxs-lookup"><span data-stu-id="e5abc-109">Math equations</span></span>
-   <span data-ttu-id="e5abc-110">Elementos do fluxograma</span><span class="sxs-lookup"><span data-stu-id="e5abc-110">Flow chart elements</span></span>

<span data-ttu-id="e5abc-111">Normalmente, os objetos que são reconhecidos por tal reconhecedor estão em uma relação espacial bidimensional ou funcional entre si.</span><span class="sxs-lookup"><span data-stu-id="e5abc-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="e5abc-112">Por exemplo, dentro das relações complexas em uma equação matemática, um reconhecedor pode retornar resultados diferentes para um limite superior em uma integral definitiva em oposição a um numerador em uma fração.</span><span class="sxs-lookup"><span data-stu-id="e5abc-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="e5abc-113">Devido à natureza muito geral dessas relações, é extremamente difícil definir o conjunto de interfaces que funcionará para cada reconhecedor de objeto.</span><span class="sxs-lookup"><span data-stu-id="e5abc-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="e5abc-114">A tecnologia do Tablet PC fornece uma estrutura básica para os reconhecedores de objetos na biblioteca gerenciada e nas interfaces de automação.</span><span class="sxs-lookup"><span data-stu-id="e5abc-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="e5abc-115">No entanto, você deve desenvolver interfaces personalizadas que descrevam relações espaciais complexas entre objetos reconhecidos para cada reconhecedor de objeto.</span><span class="sxs-lookup"><span data-stu-id="e5abc-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="e5abc-116">Especificamente, para os reconhecedores de objetos, a plataforma fornece o objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para associar o objeto de [**tinta**](inkdisp-class.md) ao contexto do reconhecedor e chamar o reconhecedor para executar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="e5abc-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



