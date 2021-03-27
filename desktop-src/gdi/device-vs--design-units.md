---
description: Um aplicativo pode recuperar as métricas de fonte para uma fonte física somente depois que a fonte tiver sido selecionada em um contexto de dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo versus unidades de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827660"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="19f24-103">Dispositivo versus unidades de design</span><span class="sxs-lookup"><span data-stu-id="19f24-103">Device vs. Design Units</span></span>

<span data-ttu-id="19f24-104">Um aplicativo pode recuperar as métricas de fonte para uma fonte física somente depois que a fonte tiver sido selecionada em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="19f24-105">Quando uma fonte é selecionada em um contexto de dispositivo, ela é dimensionada para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="19f24-106">As métricas de fonte específicas para o dispositivo são conhecidas como unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="19f24-107">As métricas portáteis em fontes são conhecidas como unidades de design.</span><span class="sxs-lookup"><span data-stu-id="19f24-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="19f24-108">Para aplicar a um dispositivo especificado, as unidades de design devem ser convertidas em unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="19f24-109">Use a fórmula a seguir para converter unidades de design em unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="19f24-110">*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*Points*/72) \* *DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="19f24-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="19f24-111">As variáveis nesta fórmula têm os seguintes significados.</span><span class="sxs-lookup"><span data-stu-id="19f24-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="19f24-112">Variável</span><span class="sxs-lookup"><span data-stu-id="19f24-112">Variable</span></span>           | <span data-ttu-id="19f24-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="19f24-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f24-114">*DeviceUnits*</span><span class="sxs-lookup"><span data-stu-id="19f24-114">*DeviceUnits*</span></span>      | <span data-ttu-id="19f24-115">Especifica a métrica de fonte *DesignUnits* convertida em unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="19f24-116">Esse valor está nas mesmas unidades que o valor especificado para *DeviceResolution*.</span><span class="sxs-lookup"><span data-stu-id="19f24-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="19f24-117">*DesignUnits*</span><span class="sxs-lookup"><span data-stu-id="19f24-117">*DesignUnits*</span></span>      | <span data-ttu-id="19f24-118">Especifica a métrica de fonte a ser convertida em unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f24-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="19f24-119">Esse valor pode ser qualquer métrica de fonte, incluindo a largura de um caractere ou o valor mais ascendente para uma fonte inteira.</span><span class="sxs-lookup"><span data-stu-id="19f24-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="19f24-120">*unitsPerEm*</span><span class="sxs-lookup"><span data-stu-id="19f24-120">*unitsPerEm*</span></span>       | <span data-ttu-id="19f24-121">Especifica o tamanho quadrado em para a fonte.</span><span class="sxs-lookup"><span data-stu-id="19f24-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="19f24-122">*Pontos*</span><span class="sxs-lookup"><span data-stu-id="19f24-122">*PointSize*</span></span>        | <span data-ttu-id="19f24-123">Especifica o tamanho da fonte, em pontos.</span><span class="sxs-lookup"><span data-stu-id="19f24-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="19f24-124">(Um ponto é igual a 1/72 de uma polegada.)</span><span class="sxs-lookup"><span data-stu-id="19f24-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="19f24-125">*DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="19f24-125">*DeviceResolution*</span></span> | <span data-ttu-id="19f24-126">Especifica o número de unidades de dispositivo (pixels) por polegada.</span><span class="sxs-lookup"><span data-stu-id="19f24-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="19f24-127">Os valores típicos podem ser 300 para uma impressora laser ou 96 para uma tela VGA.</span><span class="sxs-lookup"><span data-stu-id="19f24-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="19f24-128">Esta fórmula não deve ser usada para converter unidades de dispositivo de volta em unidades de design.</span><span class="sxs-lookup"><span data-stu-id="19f24-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="19f24-129">As unidades de dispositivo são sempre arredondadas para o pixel mais próximo.</span><span class="sxs-lookup"><span data-stu-id="19f24-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="19f24-130">O erro de arredondamento propagado pode se tornar muito grande, especialmente quando um aplicativo está trabalhando com tamanhos de tela.</span><span class="sxs-lookup"><span data-stu-id="19f24-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="19f24-131">Para solicitar unidades de design, crie uma fonte lógica cuja altura seja especificada como *unitsPerEm*.</span><span class="sxs-lookup"><span data-stu-id="19f24-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="19f24-132">Os aplicativos podem recuperar o valor de *unitsPerEm* chamando a função [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) e verificando o membro **ntmSizeEM** da estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="19f24-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



