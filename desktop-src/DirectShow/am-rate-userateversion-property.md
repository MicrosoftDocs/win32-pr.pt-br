---
description: Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Propriedade AM_RATE_UseRateVersion (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910214"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="e5b1f-103">Propriedade de UseRateVersion da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e5b1f-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="e5b1f-104">Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="e5b1f-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="e5b1f-105">O valor é um tipo de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="e5b1f-105">The value is a **WORD** type.</span></span> <span data-ttu-id="e5b1f-106">O byte de ordem superior contém o número de versão secundária e o byte de ordem inferior contém o byte de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="e5b1f-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="e5b1f-107">Assim, a versão 1,1 é sinalizada com o valor 0x0101.</span><span class="sxs-lookup"><span data-stu-id="e5b1f-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="e5b1f-108">Se o decodificador não oferecer suporte à versão especificada, ele deverá falhar na chamada para [**IKsPropertySet:: Set**](ikspropertyset-set.md) e retornar e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="e5b1f-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="e5b1f-109">Se o filtro de origem não definir a versão, o decodificador deverá ser padronizado para a versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="e5b1f-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="e5b1f-110">Label</span><span class="sxs-lookup"><span data-stu-id="e5b1f-110">Label</span></span> | <span data-ttu-id="e5b1f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b1f-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="e5b1f-112">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5b1f-112">Property Set GUID</span></span> | <span data-ttu-id="e5b1f-113">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e5b1f-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e5b1f-114">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="e5b1f-114">Property ID</span></span>       | <span data-ttu-id="e5b1f-115">\_UseRateVersion de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e5b1f-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="e5b1f-116">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e5b1f-116">Data Type</span></span>         | <span data-ttu-id="e5b1f-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="e5b1f-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="e5b1f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b1f-118">Requirements</span></span>



| <span data-ttu-id="e5b1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b1f-119">Requirement</span></span> | <span data-ttu-id="e5b1f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b1f-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b1f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5b1f-121">Header</span></span><br/> | <dl> <span data-ttu-id="e5b1f-122"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b1f-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b1f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b1f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b1f-124">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="e5b1f-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




