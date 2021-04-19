---
description: Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Propriedade AM_RATE_UseRateVersion (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771677"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="e392f-103">Propriedade de UseRateVersion da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e392f-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="e392f-104">Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="e392f-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="e392f-105">O valor é um tipo de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="e392f-105">The value is a **WORD** type.</span></span> <span data-ttu-id="e392f-106">O byte de ordem superior contém o número de versão secundária e o byte de ordem inferior contém o byte de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="e392f-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="e392f-107">Assim, a versão 1,1 é sinalizada com o valor 0x0101.</span><span class="sxs-lookup"><span data-stu-id="e392f-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="e392f-108">Se o decodificador não oferecer suporte à versão especificada, ele deverá falhar na chamada para [**IKsPropertySet:: Set**](ikspropertyset-set.md) e retornar e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="e392f-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="e392f-109">Se o filtro de origem não definir a versão, o decodificador deverá ser padronizado para a versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="e392f-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="e392f-110">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="e392f-110">Property Set GUID</span></span> | <span data-ttu-id="e392f-111">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e392f-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e392f-112">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="e392f-112">Property ID</span></span>       | <span data-ttu-id="e392f-113">\_UseRateVersion de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e392f-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="e392f-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e392f-114">Data Type</span></span>         | <span data-ttu-id="e392f-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="e392f-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="e392f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e392f-116">Requirements</span></span>



| <span data-ttu-id="e392f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e392f-117">Requirement</span></span> | <span data-ttu-id="e392f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e392f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e392f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e392f-119">Header</span></span><br/> | <dl> <span data-ttu-id="e392f-120"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e392f-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e392f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e392f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e392f-122">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="e392f-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




