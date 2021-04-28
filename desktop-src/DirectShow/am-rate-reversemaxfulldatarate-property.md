---
description: Propriedade AM_RATE_ReverseMaxFullDataRate – aplica-se ao Windows Vista e posterior.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propriedade AM_RATE_ReverseMaxFullDataRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099964"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="5c1ca-103">Propriedade de ReverseMaxFullDataRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="5c1ca-104">Aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="5c1ca-105">Retorna a taxa máxima de reprodução inversa do decodificador.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="5c1ca-106">O valor da propriedade é o valor absoluto da velocidade de inversa máxima x 10000.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="5c1ca-107">Por exemplo, se a velocidade inversa máxima for-2,0, o valor dessa propriedade será 20000.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="5c1ca-108">O tipo de dados para essa propriedade **é \_ MaxFullDataRate**, que é um `typedef` para **longo**.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="5c1ca-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-109">This property is read-only.</span></span>



| <span data-ttu-id="5c1ca-110">Label</span><span class="sxs-lookup"><span data-stu-id="5c1ca-110">Label</span></span> | <span data-ttu-id="5c1ca-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5c1ca-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="5c1ca-112">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c1ca-112">Property Set GUID</span></span> | <span data-ttu-id="5c1ca-113">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="5c1ca-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="5c1ca-114">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="5c1ca-114">Property ID</span></span>       | <span data-ttu-id="5c1ca-115">\_ReverseMaxFullDataRate de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="5c1ca-116">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5c1ca-116">Data Type</span></span>         | <span data-ttu-id="5c1ca-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="5c1ca-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="5c1ca-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c1ca-118">Remarks</span></span>

<span data-ttu-id="5c1ca-119">Os decodificadores que dão suporte à reprodução reversa suave devem expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="5c1ca-120">Para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="5c1ca-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c1ca-121">Requirements</span></span>



| <span data-ttu-id="5c1ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c1ca-122">Requirement</span></span> | <span data-ttu-id="5c1ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5c1ca-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1ca-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c1ca-124">Header</span></span><br/> | <dl> <span data-ttu-id="5c1ca-125"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1ca-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c1ca-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5c1ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1ca-127">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="5c1ca-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




