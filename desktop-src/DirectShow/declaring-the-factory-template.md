---
description: Declarando o modelo de fábrica
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Declarando o modelo de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087330"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="557e2-103">Declarando o modelo de fábrica</span><span class="sxs-lookup"><span data-stu-id="557e2-103">Declaring the Factory Template</span></span>

<span data-ttu-id="557e2-104">A próxima etapa é declarar o modelo de fábrica para seu filtro.</span><span class="sxs-lookup"><span data-stu-id="557e2-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="557e2-105">Um modelo de fábrica é uma classe C++ que contém informações para a fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="557e2-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="557e2-106">Em sua DLL, declare uma matriz global de objetos [**CFactoryTemplate**](cfactorytemplate.md) , uma para cada filtro ou componente com em sua dll.</span><span class="sxs-lookup"><span data-stu-id="557e2-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="557e2-107">A matriz deve ser nomeada *para \_ modelos g*.</span><span class="sxs-lookup"><span data-stu-id="557e2-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="557e2-108">Para obter mais informações sobre modelos de fábrica, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="557e2-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="557e2-109">O membro de **\_ \_ filtro m pAMovieSetup** do modelo de fábrica é um ponteiro para a estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="557e2-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="557e2-110">O exemplo a seguir mostra um modelo de fábrica, usando a estrutura fornecida no exemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="557e2-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="557e2-111">Se você não declarou nenhuma informação de filtro, **o \_ \_ filtro m PAMoveSetup** pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="557e2-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="557e2-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="557e2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="557e2-113">Como registrar filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="557e2-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



