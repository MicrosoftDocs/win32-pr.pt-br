---
description: As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propriedades de subimagem de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909084"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="c1a52-103">Conjunto de propriedades de subimagem de DVD</span><span class="sxs-lookup"><span data-stu-id="c1a52-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="c1a52-104">As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.</span><span class="sxs-lookup"><span data-stu-id="c1a52-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="c1a52-105">As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a52-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="c1a52-106">Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="c1a52-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="c1a52-107">Label</span><span class="sxs-lookup"><span data-stu-id="c1a52-107">Label</span></span> | <span data-ttu-id="c1a52-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c1a52-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="c1a52-109">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1a52-109">Property Set GUID</span></span> | <span data-ttu-id="c1a52-110">\_KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="c1a52-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="c1a52-111">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c1a52-111">Property ID</span></span>                           | <span data-ttu-id="c1a52-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1a52-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a52-113">\_ \_ \_ composição \_ de DVDSUBPIC da propriedade am</span><span class="sxs-lookup"><span data-stu-id="c1a52-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="c1a52-114">Propriedade somente definição que habilita ou desabilita a exibição de subimagem.</span><span class="sxs-lookup"><span data-stu-id="c1a52-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="c1a52-115">O DirectShow define **a \_ composição da propriedade am \_ \_ no** tipo de dados booliano para essa propriedade, bem como a \_ composição da propriedade \_ do Pam \_ como um ponteiro para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c1a52-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="c1a52-116">**Verdadeiro** indica que a subimagem é exibida, **falso** indica desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="c1a52-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="c1a52-117">Consulte a parte WDM do Windows DDK para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c1a52-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="c1a52-118">\_Propriedade am \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="c1a52-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="c1a52-119">Propriedade somente definição que especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado.</span><span class="sxs-lookup"><span data-stu-id="c1a52-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="c1a52-120">O tipo de dados é [**\_ propriedade \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="c1a52-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="c1a52-121">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="c1a52-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="c1a52-122">\_ \_ paleta DVDSUBPIC da propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="c1a52-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="c1a52-123">Define a paleta para uma subimagem.</span><span class="sxs-lookup"><span data-stu-id="c1a52-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="c1a52-124">O tipo de dados é [**\_ propriedade \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="c1a52-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c1a52-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1a52-125">Remarks</span></span>

<span data-ttu-id="c1a52-126">A propriedade **am da \_ propriedade \_ DVDSUBPIC \_ HLI** é somente definido.</span><span class="sxs-lookup"><span data-stu-id="c1a52-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="c1a52-127">Especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado.</span><span class="sxs-lookup"><span data-stu-id="c1a52-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="c1a52-128">Isso difere da especificação de DVD-Video, pois o navegador de DVD da Microsoft analisa todas as informações de botão e teclado e passa apenas um retângulo de realce para o decodificador de subimagem em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="c1a52-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="c1a52-129">Como resultado, as informações de realce são enviadas para o decodificador com mais frequência do que está presente no fluxo de DVD.</span><span class="sxs-lookup"><span data-stu-id="c1a52-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="c1a52-130">As informações de realce chegam de forma assíncrona ao fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c1a52-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="c1a52-131">O decodificador usa os carimbos de data e hora de início e término para correlacionar as informações de realce às informações relevantes da subimagem, se houver.</span><span class="sxs-lookup"><span data-stu-id="c1a52-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="c1a52-132">Se o decodificador não recebeu nenhuma informação de fluxo de subimagem para os carimbos de data/hora solicitados, o decodificador supõe que as informações de realce são autônomas e não se aplicam a uma subimagem.</span><span class="sxs-lookup"><span data-stu-id="c1a52-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="c1a52-133">Nesse caso, o decodificador assume que as informações de cor e contraste têm a mesma cor.</span><span class="sxs-lookup"><span data-stu-id="c1a52-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="c1a52-134">Os dados não estão totalmente no formato de disco DVD.</span><span class="sxs-lookup"><span data-stu-id="c1a52-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="c1a52-135">A Microsoft fornece uma estrutura adicional da [**Propriedade Type am \_ \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) que é passada como o parâmetro para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c1a52-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="c1a52-136">Esta estrutura descreve o botão atualmente selecionado das informações de realce de DVD.</span><span class="sxs-lookup"><span data-stu-id="c1a52-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="c1a52-137">O navegador de DVD processa todas as informações de pressionamento de tecla e envia novas informações de realce sempre que um estado de botão é alterado.</span><span class="sxs-lookup"><span data-stu-id="c1a52-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="c1a52-138">As informações descrevem apenas um modo de um botão por vez.</span><span class="sxs-lookup"><span data-stu-id="c1a52-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="c1a52-139">Ele inclui um retângulo de exibição em coordenadas de pixel da tela ou uma exibição da subimagem, se presente.</span><span class="sxs-lookup"><span data-stu-id="c1a52-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="c1a52-140">A estrutura também contém informações de cor e contraste, mas apenas para o estado atual do botão atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="c1a52-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="c1a52-141">O formato é definido na especificação de DVD.</span><span class="sxs-lookup"><span data-stu-id="c1a52-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="c1a52-142">Informações de realce contêm carimbos de data/hora de início e término.</span><span class="sxs-lookup"><span data-stu-id="c1a52-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="c1a52-143">Elas estão nas mesmas unidades que outros carimbos de data/hora, com duas exceções: um carimbo de data/hora de início de 0xFFFFFFFF significa que a propriedade de realce é efetivada após o recebimento e um carimbo de hora de término de 0xFFFFFFFF significa que a propriedade realce é válida até que o próximo realce seja recebido.</span><span class="sxs-lookup"><span data-stu-id="c1a52-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="c1a52-144">O campo HLISS é conforme definido na especificação do DVD.</span><span class="sxs-lookup"><span data-stu-id="c1a52-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="c1a52-145">Um valor de zero indica que todos os realces são inválidos e o decodificador deve desabilitar todos os realces.</span><span class="sxs-lookup"><span data-stu-id="c1a52-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a52-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1a52-146">Requirements</span></span>



| <span data-ttu-id="c1a52-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1a52-147">Requirement</span></span> | <span data-ttu-id="c1a52-148">Valor</span><span class="sxs-lookup"><span data-stu-id="c1a52-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a52-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1a52-149">Header</span></span><br/> | <dl> <span data-ttu-id="c1a52-150"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a52-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a52-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1a52-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a52-152">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="c1a52-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




