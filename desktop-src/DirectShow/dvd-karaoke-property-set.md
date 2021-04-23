---
description: Quando o filtro de navegador de DVD entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propriedades de karaokê de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909064"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="5aad3-103">Conjunto de propriedades de karaokê de DVD</span><span class="sxs-lookup"><span data-stu-id="5aad3-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="5aad3-104">Quando o filtro de [navegador de DVD](dvd-navigator-filter.md) entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade **am \_ \_ DVDKARAOKE \_ Enable** Property.</span><span class="sxs-lookup"><span data-stu-id="5aad3-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="5aad3-105">O decodificador deve ativar mudo dos canais de áudio de 2 a 5 até que ele receba do navegador de DVD uma propriedade **am \_ \_ DVDKARAOKE \_ data de propriedade** com um ponteiro para uma estrutura de dados [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indicando como os canais auxiliares devem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="5aad3-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="5aad3-106">Label</span><span class="sxs-lookup"><span data-stu-id="5aad3-106">Label</span></span> | <span data-ttu-id="5aad3-107">Valor</span><span class="sxs-lookup"><span data-stu-id="5aad3-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="5aad3-108">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="5aad3-108">Property Set GUID</span></span> | <span data-ttu-id="5aad3-109">\_KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="5aad3-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="5aad3-110">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="5aad3-110">Property ID</span></span>                      | <span data-ttu-id="5aad3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5aad3-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aad3-112">\_ \_ habilitar DVDKARAOKE de propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="5aad3-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="5aad3-113">Valor BOOLIANo.</span><span class="sxs-lookup"><span data-stu-id="5aad3-113">BOOLEAN value.</span></span> <span data-ttu-id="5aad3-114">O navegador de DVD envia o decodificador que uma \_ Propriedade am \_ DVDKARAOKE \_ habilita com um valor de **true** para habilitar o karaokê downmixing ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="5aad3-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="5aad3-115">\_dados da propriedade am \_ DVDKARAOKE \_</span><span class="sxs-lookup"><span data-stu-id="5aad3-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="5aad3-116">O navegador de DVD envia o decodificador uma \_ propriedade de dados DVDKARAOKE de propriedade am \_ \_ com um ponteiro para uma estrutura [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) para alterar a configuração de downmix, ou seja, para ativar ou desativar determinados canais de karaokê e direcioná-los para o canal de saída à direita ou à esquerda.</span><span class="sxs-lookup"><span data-stu-id="5aad3-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5aad3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aad3-117">Requirements</span></span>



| <span data-ttu-id="5aad3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aad3-118">Requirement</span></span> | <span data-ttu-id="5aad3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5aad3-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5aad3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5aad3-120">Header</span></span><br/> | <dl> <span data-ttu-id="5aad3-121"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aad3-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aad3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5aad3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aad3-123">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="5aad3-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




