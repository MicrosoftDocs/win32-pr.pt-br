---
title: Identificadores de tipo de espaço de cores
description: Essas constantes especificam o tipo de uma matriz de espaço de cores de PostScript 2. Os valores a seguir são tipos de matriz de espaço de cores válidos.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105795511"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="d3b55-104">Identificadores de tipo de espaço de cores</span><span class="sxs-lookup"><span data-stu-id="d3b55-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="d3b55-105">Essas constantes especificam o tipo de uma matriz de espaço de cores de PostScript 2.</span><span class="sxs-lookup"><span data-stu-id="d3b55-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="d3b55-106">Os valores a seguir são tipos de matriz de espaço de cores válidos.</span><span class="sxs-lookup"><span data-stu-id="d3b55-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="d3b55-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="d3b55-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-108">Obtenha uma matriz de espaço de cores CIEBasedA do perfil monocromático.</span><span class="sxs-lookup"><span data-stu-id="d3b55-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_cinza CSA**</span><span class="sxs-lookup"><span data-stu-id="d3b55-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-110">Obtenha uma matriz de espaço de cores CIEBasedA do perfil monocromático.</span><span class="sxs-lookup"><span data-stu-id="d3b55-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**ABC de CSA \_**</span><span class="sxs-lookup"><span data-stu-id="d3b55-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-112">Obtenha uma matriz de espaço de cores CIEBasedABC do perfil RGB ou L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="d3b55-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**definição de CSA \_**</span><span class="sxs-lookup"><span data-stu-id="d3b55-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-114">Obtenha uma matriz de espaço de cores CIEBasedDEF do perfil RGB ou L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="d3b55-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**do CSA \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="d3b55-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-116">Obtenha uma matriz de espaço de cores CIEBasedDEF seguida por uma matriz de espaço de cores CIEBasedABC do perfil RGB.</span><span class="sxs-lookup"><span data-stu-id="d3b55-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="d3b55-117">Na execução, se a impressora não der suporte a espaços de cores CIEBasedDEF, a função usará a definição CIEBasedABC.</span><span class="sxs-lookup"><span data-stu-id="d3b55-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratório CSA**</span><span class="sxs-lookup"><span data-stu-id="d3b55-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-119">Obtém uma matriz de espaço de cores CIEBasedABC do <sup>\*</sup> perfil L a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="d3b55-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_DEFG CSA**</span><span class="sxs-lookup"><span data-stu-id="d3b55-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-121">Obtenha uma matriz de espaço de cores CIEBasedDEFG do perfil CMYK.</span><span class="sxs-lookup"><span data-stu-id="d3b55-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3b55-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**</span><span class="sxs-lookup"><span data-stu-id="d3b55-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d3b55-123">Obtenha uma matriz de espaço de cores CIEBasedCMYK do perfil CMYK.</span><span class="sxs-lookup"><span data-stu-id="d3b55-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d3b55-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3b55-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b55-125">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="d3b55-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="d3b55-126">Constantes de ICM</span><span class="sxs-lookup"><span data-stu-id="d3b55-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




