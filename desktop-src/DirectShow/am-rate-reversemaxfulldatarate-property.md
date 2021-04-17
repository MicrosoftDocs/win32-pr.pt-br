---
description: Aplica-se ao Windows Vista e posterior.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propriedade AM_RATE_ReverseMaxFullDataRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749055"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="ac4e8-103">Propriedade de ReverseMaxFullDataRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="ac4e8-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="ac4e8-104">Aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="ac4e8-105">Retorna a taxa máxima de reprodução inversa do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="ac4e8-106">O valor da propriedade é o valor absoluto da velocidade de inversa máxima x 10000.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="ac4e8-107">Por exemplo, se a velocidade inversa máxima for-2,0, o valor dessa propriedade será 20000.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="ac4e8-108">O tipo de dados para essa propriedade **é \_ MaxFullDataRate**, que é um `typedef` para **longo**.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="ac4e8-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="ac4e8-110">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac4e8-110">Property Set GUID</span></span> | <span data-ttu-id="ac4e8-111">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="ac4e8-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="ac4e8-112">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ac4e8-112">Property ID</span></span>       | <span data-ttu-id="ac4e8-113">\_ReverseMaxFullDataRate de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="ac4e8-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="ac4e8-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ac4e8-114">Data Type</span></span>         | <span data-ttu-id="ac4e8-115">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="ac4e8-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="ac4e8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac4e8-116">Remarks</span></span>

<span data-ttu-id="ac4e8-117">Os decodificadores que dão suporte à reprodução reversa suave devem expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="ac4e8-118">Para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="ac4e8-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4e8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac4e8-119">Requirements</span></span>



| <span data-ttu-id="ac4e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac4e8-120">Requirement</span></span> | <span data-ttu-id="ac4e8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ac4e8-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4e8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac4e8-122">Header</span></span><br/> | <dl> <span data-ttu-id="ac4e8-123"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4e8-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4e8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac4e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4e8-125">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="ac4e8-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




