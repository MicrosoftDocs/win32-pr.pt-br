---
title: 'sRGB: um espaço de cores padrão'
description: Como resultado das considerações sobre largura de banda da Internet, a Hewlett-Packard e a Microsoft proempção de um espaço de cores predefinido padrão conhecido como sRGB (IEC 61966-2-1), de modo a permitir mapeamento de cores preciso com pouca sobrecarga de dados.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- WCS (Sistema de Cores do Windows), espaço de cor sRGB
- WCS (Sistema de Cores do Windows), espaço de cor sRGB
- gerenciamento de cores da imagem, espaço de cor sRGB
- gerenciamento de cores, espaço de cor sRGB
- colors,sRGB color space
- Espaço de cor sRGB
- espaços de cores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443637"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="e9525-110">sRGB: um espaço de cor padrão</span><span class="sxs-lookup"><span data-stu-id="e9525-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="e9525-111">Como resultado das considerações sobre largura de banda da Internet, o [](c.md) Hewlett-Packard e a Microsoft proempção de um espaço de cores predefinido padrão [](c.md) conhecido como *sRGB* (IEC 61966-2-1), de modo a permitir o mapeamento de cores preciso com muito pouca sobrecarga de dados.</span><span class="sxs-lookup"><span data-stu-id="e9525-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="e9525-112">Uma versão do arquivo de ajuda de um white paper que discute os detalhes técnicos de sRGB, sRGB.hlp, está disponível na pasta Ajuda da Referência do Programador do \\ WCS 1.0.</span><span class="sxs-lookup"><span data-stu-id="e9525-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="e9525-113">Formatos de arquivo diferentes podem usar ou adicionar um sinalizador para especificar que a imagem está no espaço de cores sRGB.</span><span class="sxs-lookup"><span data-stu-id="e9525-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="e9525-114">No formato DIB (bitmap independente de dispositivo) do Windows, definir o membro **bV5CSType** da estrutura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) como **\_ LCS sRGB** especifica que as cores DIB estão no espaço de cores sRGB.</span><span class="sxs-lookup"><span data-stu-id="e9525-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="e9525-115">O WCS 1.0 fornece suporte nativo para sRGB.</span><span class="sxs-lookup"><span data-stu-id="e9525-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="e9525-116">Há duas maneiras de usar o WCS 1.0 para renderizar uma imagem definida no espaço de cores sRGB:</span><span class="sxs-lookup"><span data-stu-id="e9525-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="e9525-117">**Para renderizar uma imagem dentro do contexto do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="e9525-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="e9525-118">Crie um DC (contexto de dispositivo) no dispositivo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9525-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="e9525-119">Definir o gerenciamento de cores usando [**a função SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)</span><span class="sxs-lookup"><span data-stu-id="e9525-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="e9525-120">Use a [**função SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir o DIB para o DC.</span><span class="sxs-lookup"><span data-stu-id="e9525-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="e9525-121">Desde que o membro **bV5CSMType** da estrutura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) de DIBs seja definido como **LCS \_ sRGB,** o sistema executará o gerenciamento de cores apropriado.</span><span class="sxs-lookup"><span data-stu-id="e9525-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="e9525-122">**Para renderizar uma imagem fora do contexto do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="e9525-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="e9525-123">Crie uma transformação usando [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw)</span><span class="sxs-lookup"><span data-stu-id="e9525-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="e9525-124">O **membro lcsCSType** da estrutura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) apontada pelo parâmetro *pLogColorSpace* deve ser definido como **LCS \_ sRGB.**</span><span class="sxs-lookup"><span data-stu-id="e9525-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="e9525-125">O *parâmetro hDestProfile* indica o espaço de cores do dispositivo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9525-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="e9525-126">Use a transformação de cor criada para corresponder à imagem antes de exibi-la no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9525-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="e9525-127">Padrões do WCS 1.0 para espaço de cor de entrada e perfil de saída</span><span class="sxs-lookup"><span data-stu-id="e9525-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="e9525-128">Quando nenhum espaço de cor de entrada é especificado, por padrão, o WCS 1.0 usa o espaço de cores sRGB como o espaço de cor de entrada para mapeamento [de cores.](c.md)</span><span class="sxs-lookup"><span data-stu-id="e9525-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="e9525-129">Quando nenhum perfil de saída é especificado, mas um dispositivo padrão é especificado, o WCS 1.0 seleciona um perfil de saída padrão.</span><span class="sxs-lookup"><span data-stu-id="e9525-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="e9525-130">Se o dispositivo padrão não tiver um perfil associado, o WCS 1.0 usará o espaço de cores sRGB como o perfil de saída.</span><span class="sxs-lookup"><span data-stu-id="e9525-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="e9525-131">A tabela a seguir mostra as transformaçãos de cor resultantes quando um dispositivo padrão não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e9525-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|  &nbsp;                               | <span data-ttu-id="e9525-132">Perfil de saída especificado</span><span class="sxs-lookup"><span data-stu-id="e9525-132">Output Profile Specified</span></span>                              | <span data-ttu-id="e9525-133">Perfil de saída não especificado</span><span class="sxs-lookup"><span data-stu-id="e9525-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e9525-134">Espaço de cor de entrada especificado</span><span class="sxs-lookup"><span data-stu-id="e9525-134">Input Color Space Specified</span></span>     | <span data-ttu-id="e9525-135">A transformação usa os perfis especificados.</span><span class="sxs-lookup"><span data-stu-id="e9525-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="e9525-136">A transformação converte do espaço de cor de entrada conhecido em sRGB.</span><span class="sxs-lookup"><span data-stu-id="e9525-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="e9525-137">Espaço de cor de entrada não especificado</span><span class="sxs-lookup"><span data-stu-id="e9525-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="e9525-138">Transforme as conversões de sRGB em perfil de saída conhecido.</span><span class="sxs-lookup"><span data-stu-id="e9525-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="e9525-139">A transformação de sRGB para sRGB é assumida; nada é feito.</span><span class="sxs-lookup"><span data-stu-id="e9525-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="e9525-140">Perfis sRGB e inseridos</span><span class="sxs-lookup"><span data-stu-id="e9525-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="e9525-141">A partir da versão 2.0 do ICM, os aplicativos que utilizam o WCS podem inserir perfis em imagens.</span><span class="sxs-lookup"><span data-stu-id="e9525-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="e9525-142">Os perfis inseridos auxiliam os aplicativos dos usuários a manter uma aparência de cor consistente, mesmo que as imagens sejam transmitidas pela Internet.</span><span class="sxs-lookup"><span data-stu-id="e9525-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="e9525-143">As imagens que usam o espaço de cores sRGB não precisam de um perfil de cor inserido.</span><span class="sxs-lookup"><span data-stu-id="e9525-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="e9525-144">Como eles não têm perfil inserido, as imagens baseadas em sRGB são menores e facilmente transferíveis entre canais de dados com largura de banda limitada.</span><span class="sxs-lookup"><span data-stu-id="e9525-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="e9525-145">Os aplicativos devem definir o sinalizador **\_ SRGB** do LCS no header de bitmap da imagem para indicar que a imagem usa o espaço de cor sRGB.</span><span class="sxs-lookup"><span data-stu-id="e9525-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="e9525-146">Para obter detalhes, consulte [Estruturas de header do Bitmap do Windows](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="e9525-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 