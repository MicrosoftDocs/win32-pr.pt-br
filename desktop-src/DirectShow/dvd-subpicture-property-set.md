---
description: As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propriedades de subimagem de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779490"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="35de9-103">Conjunto de propriedades de subimagem de DVD</span><span class="sxs-lookup"><span data-stu-id="35de9-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="35de9-104">As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.</span><span class="sxs-lookup"><span data-stu-id="35de9-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="35de9-105">As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="35de9-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="35de9-106">Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="35de9-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="35de9-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="35de9-107">Property Set GUID</span></span> | <span data-ttu-id="35de9-108">\_KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="35de9-108">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="35de9-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="35de9-109">Property ID</span></span>                           | <span data-ttu-id="35de9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35de9-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35de9-111">\_ \_ \_ composição \_ de DVDSUBPIC da propriedade am</span><span class="sxs-lookup"><span data-stu-id="35de9-111">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="35de9-112">Propriedade somente definição que habilita ou desabilita a exibição de subimagem.</span><span class="sxs-lookup"><span data-stu-id="35de9-112">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="35de9-113">O DirectShow define **a \_ composição da propriedade am \_ \_ no** tipo de dados booliano para essa propriedade, bem como a \_ composição da propriedade \_ do Pam \_ como um ponteiro para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="35de9-113">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="35de9-114">**Verdadeiro** indica que a subimagem é exibida, **falso** indica desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="35de9-114">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="35de9-115">Consulte a parte WDM do Windows DDK para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="35de9-115">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="35de9-116">\_Propriedade am \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="35de9-116">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="35de9-117">Propriedade somente definição que especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado.</span><span class="sxs-lookup"><span data-stu-id="35de9-117">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="35de9-118">O tipo de dados é [**\_ propriedade \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="35de9-118">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="35de9-119">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="35de9-119">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="35de9-120">\_ \_ paleta DVDSUBPIC da propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="35de9-120">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="35de9-121">Define a paleta para uma subimagem.</span><span class="sxs-lookup"><span data-stu-id="35de9-121">Sets the palette for a subpicture.</span></span> <span data-ttu-id="35de9-122">O tipo de dados é [**\_ propriedade \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="35de9-122">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="35de9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35de9-123">Remarks</span></span>

<span data-ttu-id="35de9-124">A propriedade **am da \_ propriedade \_ DVDSUBPIC \_ HLI** é somente definido.</span><span class="sxs-lookup"><span data-stu-id="35de9-124">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="35de9-125">Especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado.</span><span class="sxs-lookup"><span data-stu-id="35de9-125">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="35de9-126">Isso difere da especificação de DVD-Video, pois o navegador de DVD da Microsoft analisa todas as informações de botão e teclado e passa apenas um retângulo de realce para o decodificador de subimagem em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="35de9-126">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="35de9-127">Como resultado, as informações de realce são enviadas para o decodificador com mais frequência do que está presente no fluxo de DVD.</span><span class="sxs-lookup"><span data-stu-id="35de9-127">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="35de9-128">As informações de realce chegam de forma assíncrona ao fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="35de9-128">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="35de9-129">O decodificador usa os carimbos de data e hora de início e término para correlacionar as informações de realce às informações relevantes da subimagem, se houver.</span><span class="sxs-lookup"><span data-stu-id="35de9-129">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="35de9-130">Se o decodificador não recebeu nenhuma informação de fluxo de subimagem para os carimbos de data/hora solicitados, o decodificador supõe que as informações de realce são autônomas e não se aplicam a uma subimagem.</span><span class="sxs-lookup"><span data-stu-id="35de9-130">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="35de9-131">Nesse caso, o decodificador assume que as informações de cor e contraste têm a mesma cor.</span><span class="sxs-lookup"><span data-stu-id="35de9-131">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="35de9-132">Os dados não estão totalmente no formato de disco DVD.</span><span class="sxs-lookup"><span data-stu-id="35de9-132">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="35de9-133">A Microsoft fornece uma estrutura adicional da [**Propriedade Type am \_ \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) que é passada como o parâmetro para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="35de9-133">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="35de9-134">Esta estrutura descreve o botão atualmente selecionado das informações de realce de DVD.</span><span class="sxs-lookup"><span data-stu-id="35de9-134">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="35de9-135">O navegador de DVD processa todas as informações de pressionamento de tecla e envia novas informações de realce sempre que um estado de botão é alterado.</span><span class="sxs-lookup"><span data-stu-id="35de9-135">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="35de9-136">As informações descrevem apenas um modo de um botão por vez.</span><span class="sxs-lookup"><span data-stu-id="35de9-136">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="35de9-137">Ele inclui um retângulo de exibição em coordenadas de pixel da tela ou uma exibição da subimagem, se presente.</span><span class="sxs-lookup"><span data-stu-id="35de9-137">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="35de9-138">A estrutura também contém informações de cor e contraste, mas apenas para o estado atual do botão atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="35de9-138">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="35de9-139">O formato é definido na especificação de DVD.</span><span class="sxs-lookup"><span data-stu-id="35de9-139">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="35de9-140">Informações de realce contêm carimbos de data/hora de início e término.</span><span class="sxs-lookup"><span data-stu-id="35de9-140">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="35de9-141">Elas estão nas mesmas unidades que outros carimbos de data/hora, com duas exceções: um carimbo de data/hora de início de 0xFFFFFFFF significa que a propriedade de realce é efetivada após o recebimento e um carimbo de hora de término de 0xFFFFFFFF significa que a propriedade realce é válida até que o próximo realce seja recebido.</span><span class="sxs-lookup"><span data-stu-id="35de9-141">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="35de9-142">O campo HLISS é conforme definido na especificação do DVD.</span><span class="sxs-lookup"><span data-stu-id="35de9-142">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="35de9-143">Um valor de zero indica que todos os realces são inválidos e o decodificador deve desabilitar todos os realces.</span><span class="sxs-lookup"><span data-stu-id="35de9-143">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="35de9-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35de9-144">Requirements</span></span>



| <span data-ttu-id="35de9-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="35de9-145">Requirement</span></span> | <span data-ttu-id="35de9-146">Valor</span><span class="sxs-lookup"><span data-stu-id="35de9-146">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35de9-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35de9-147">Header</span></span><br/> | <dl> <span data-ttu-id="35de9-148"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="35de9-148"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35de9-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="35de9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35de9-150">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="35de9-150">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




