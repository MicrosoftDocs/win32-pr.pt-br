---
description: O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propriedade AM_RATE_CorrectTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910294"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="13d25-103">Propriedade de CorrectTS da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="13d25-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="13d25-104">O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.</span><span class="sxs-lookup"><span data-stu-id="13d25-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="13d25-105">Label</span><span class="sxs-lookup"><span data-stu-id="13d25-105">Label</span></span> | <span data-ttu-id="13d25-106">Valor</span><span class="sxs-lookup"><span data-stu-id="13d25-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="13d25-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="13d25-107">Property Set GUID</span></span> | <span data-ttu-id="13d25-108">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="13d25-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="13d25-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="13d25-109">Property ID</span></span>       | <span data-ttu-id="13d25-110">\_CorrectTS de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="13d25-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="13d25-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="13d25-111">Data Type</span></span>         | <span data-ttu-id="13d25-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="13d25-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="13d25-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d25-113">Remarks</span></span>

<span data-ttu-id="13d25-114">As versões anteriores do navegador de DVD não definiram os carimbos de data/hora corretos quando a taxa de reprodução era algo diferente de 1,0.</span><span class="sxs-lookup"><span data-stu-id="13d25-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="13d25-115">Muitos decodificadores configuram esse problema ignorando os carimbos de data/hora durante o retrocesso ou avanço rápido e Estimando os tempos de apresentação corretos.</span><span class="sxs-lookup"><span data-stu-id="13d25-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="13d25-116">Esses problemas foram corrigidos na versão atual do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="13d25-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="13d25-117">Para compatibilidade com versões anteriores com decodificadores existentes, o navegador de DVD indica que os carimbos de data/hora estão corretos, definindo a \_ Propriedade CorrectTS da taxa de am \_ no decodificador com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="13d25-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="13d25-118">Quando essa propriedade é definida, o decodificador deve usar os carimbos de data/hora reais, em vez de estimar os tempos de apresentação.</span><span class="sxs-lookup"><span data-stu-id="13d25-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d25-119">Requirements</span></span>



| <span data-ttu-id="13d25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d25-120">Requirement</span></span> | <span data-ttu-id="13d25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="13d25-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13d25-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13d25-122">Header</span></span><br/> | <dl> <span data-ttu-id="13d25-123"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="13d25-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d25-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d25-125">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="13d25-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




