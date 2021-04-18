---
title: Alterando predefinições
description: Alterando predefinições
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizações, exemplo de brilho
- visualizações personalizadas, exemplo de brilho
- Guia de programação, visualizações
- amostras, visualização de brilho
- Exemplo de visualização de brilho
- visualizações, predefinições
- visualizações personalizadas, predefinições
- predefinições em visualizações, exemplo de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759735"
---
# <a name="changing-presets"></a><span data-ttu-id="d1ca3-111">Alterando predefinições</span><span class="sxs-lookup"><span data-stu-id="d1ca3-111">Changing Presets</span></span>

<span data-ttu-id="d1ca3-112">As seções de código predefinida a seguir foram alteradas para permitir três predefinições:</span><span class="sxs-lookup"><span data-stu-id="d1ca3-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="d1ca3-113">GetPresetTitle</span><span class="sxs-lookup"><span data-stu-id="d1ca3-113">GetPresetTitle</span></span>

<span data-ttu-id="d1ca3-114">Esse código foi inserido no lugar do código predefinido gerado:</span><span class="sxs-lookup"><span data-stu-id="d1ca3-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="d1ca3-115">Enumerações</span><span class="sxs-lookup"><span data-stu-id="d1ca3-115">Enumerations</span></span>

<span data-ttu-id="d1ca3-116">A seguinte enumeração em brilho. h foi alterada para permitir três predefinições:</span><span class="sxs-lookup"><span data-stu-id="d1ca3-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="d1ca3-117">Cabeçalho do recurso</span><span class="sxs-lookup"><span data-stu-id="d1ca3-117">Resource Header</span></span>

<span data-ttu-id="d1ca3-118">Os recursos a seguir foram definidos em Resource. h para permitir três predefinições:</span><span class="sxs-lookup"><span data-stu-id="d1ca3-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="d1ca3-119">Observe que você também deve alterar o número do recurso do **\_ APS \_ próximo \_ \_ valor SYMED** para 106.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="d1ca3-120">Arquivo de recurso</span><span class="sxs-lookup"><span data-stu-id="d1ca3-120">Resource File</span></span>

<span data-ttu-id="d1ca3-121">As cadeias de caracteres a seguir devem ser alteradas no arquivo Glowdll. rc para permitir três predefinições e dar a eles nomes:</span><span class="sxs-lookup"><span data-stu-id="d1ca3-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="d1ca3-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1ca3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ca3-123">**O exemplo de brilho**</span><span class="sxs-lookup"><span data-stu-id="d1ca3-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




