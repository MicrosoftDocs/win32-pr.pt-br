---
description: Quando o filtro de navegador de DVD entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propriedades de karaokê de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780637"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="c9c27-103">Conjunto de propriedades de karaokê de DVD</span><span class="sxs-lookup"><span data-stu-id="c9c27-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="c9c27-104">Quando o filtro de [navegador de DVD](dvd-navigator-filter.md) entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade **am \_ \_ DVDKARAOKE \_ Enable** Property.</span><span class="sxs-lookup"><span data-stu-id="c9c27-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="c9c27-105">O decodificador deve ativar mudo dos canais de áudio de 2 a 5 até que ele receba do navegador de DVD uma propriedade **am \_ \_ DVDKARAOKE \_ data de propriedade** com um ponteiro para uma estrutura de dados [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indicando como os canais auxiliares devem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="c9c27-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



|                   |                             |
|-------------------|-----------------------------|
| <span data-ttu-id="c9c27-106">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9c27-106">Property Set GUID</span></span> | <span data-ttu-id="c9c27-107">\_KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="c9c27-107">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="c9c27-108">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c9c27-108">Property ID</span></span>                      | <span data-ttu-id="c9c27-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9c27-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c27-110">\_ \_ habilitar DVDKARAOKE de propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="c9c27-110">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="c9c27-111">Valor BOOLIANo.</span><span class="sxs-lookup"><span data-stu-id="c9c27-111">BOOLEAN value.</span></span> <span data-ttu-id="c9c27-112">O navegador de DVD envia o decodificador que uma \_ Propriedade am \_ DVDKARAOKE \_ habilita com um valor de **true** para habilitar o karaokê downmixing ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="c9c27-112">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="c9c27-113">\_dados da propriedade am \_ DVDKARAOKE \_</span><span class="sxs-lookup"><span data-stu-id="c9c27-113">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="c9c27-114">O navegador de DVD envia o decodificador uma \_ propriedade de dados DVDKARAOKE de propriedade am \_ \_ com um ponteiro para uma estrutura [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) para alterar a configuração de downmix, ou seja, para ativar ou desativar determinados canais de karaokê e direcioná-los para o canal de saída à direita ou à esquerda.</span><span class="sxs-lookup"><span data-stu-id="c9c27-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c9c27-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9c27-115">Requirements</span></span>



| <span data-ttu-id="c9c27-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9c27-116">Requirement</span></span> | <span data-ttu-id="c9c27-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c9c27-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c27-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9c27-118">Header</span></span><br/> | <dl> <span data-ttu-id="c9c27-119"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c27-119"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9c27-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9c27-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c27-121">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="c9c27-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




