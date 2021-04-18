---
description: O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propriedade AM_RATE_CorrectTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810956"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="b5a27-103">Propriedade de CorrectTS da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="b5a27-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="b5a27-104">O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.</span><span class="sxs-lookup"><span data-stu-id="b5a27-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="b5a27-105">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5a27-105">Property Set GUID</span></span> | <span data-ttu-id="b5a27-106">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="b5a27-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="b5a27-107">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="b5a27-107">Property ID</span></span>       | <span data-ttu-id="b5a27-108">\_CorrectTS de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="b5a27-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="b5a27-109">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="b5a27-109">Data Type</span></span>         | <span data-ttu-id="b5a27-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="b5a27-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="b5a27-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5a27-111">Remarks</span></span>

<span data-ttu-id="b5a27-112">As versões anteriores do navegador de DVD não definiram os carimbos de data/hora corretos quando a taxa de reprodução era algo diferente de 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5a27-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="b5a27-113">Muitos decodificadores configuram esse problema ignorando os carimbos de data/hora durante o retrocesso ou avanço rápido e Estimando os tempos de apresentação corretos.</span><span class="sxs-lookup"><span data-stu-id="b5a27-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="b5a27-114">Esses problemas foram corrigidos na versão atual do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="b5a27-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="b5a27-115">Para compatibilidade com versões anteriores com decodificadores existentes, o navegador de DVD indica que os carimbos de data/hora estão corretos, definindo a \_ Propriedade CorrectTS da taxa de am \_ no decodificador com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="b5a27-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="b5a27-116">Quando essa propriedade é definida, o decodificador deve usar os carimbos de data/hora reais, em vez de estimar os tempos de apresentação.</span><span class="sxs-lookup"><span data-stu-id="b5a27-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a27-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a27-117">Requirements</span></span>



| <span data-ttu-id="b5a27-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a27-118">Requirement</span></span> | <span data-ttu-id="b5a27-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a27-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a27-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5a27-120">Header</span></span><br/> | <dl> <span data-ttu-id="b5a27-121"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a27-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a27-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5a27-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a27-123">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="b5a27-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




