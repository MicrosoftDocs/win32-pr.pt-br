---
description: Aplica-se ao Windows Vista e posterior.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Propriedade AM_RATE_ResetOnTimeDisc (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910244"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="9d65d-103">Propriedade de ResetOnTimeDisc da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="9d65d-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="9d65d-104">Aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="9d65d-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="9d65d-105">Essa propriedade consulta se o decodificador ressincroniza os carimbos de hora de saída para os carimbos de hora de entrada quando o decodificador recebe um exemplo com o sinalizador de descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="9d65d-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="9d65d-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9d65d-106">This property is read/write.</span></span>



| <span data-ttu-id="9d65d-107">Label</span><span class="sxs-lookup"><span data-stu-id="9d65d-107">Label</span></span> | <span data-ttu-id="9d65d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9d65d-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="9d65d-109">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d65d-109">Property Set GUID</span></span> | <span data-ttu-id="9d65d-110">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="9d65d-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="9d65d-111">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="9d65d-111">Property ID</span></span>       | <span data-ttu-id="9d65d-112">\_ResetOnTimeDisc de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="9d65d-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="9d65d-113">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="9d65d-113">Data Type</span></span>         | <span data-ttu-id="9d65d-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9d65d-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="9d65d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d65d-115">Remarks</span></span>

<span data-ttu-id="9d65d-116">Esta propriedade dá suporte a alterações de taxa suave.</span><span class="sxs-lookup"><span data-stu-id="9d65d-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="9d65d-117">Se o valor dessa propriedade for **true** e o decodificador receber um exemplo de entrada com o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, o quadro decodificado deverá ter o mesmo carimbo de data/hora que o quadro de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d65d-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="9d65d-118">Para recuperar o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo.</span><span class="sxs-lookup"><span data-stu-id="9d65d-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="9d65d-119">O sinalizador é definido no membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="9d65d-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="9d65d-120">Para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="9d65d-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d65d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d65d-121">Requirements</span></span>



| <span data-ttu-id="9d65d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d65d-122">Requirement</span></span> | <span data-ttu-id="9d65d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9d65d-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d65d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d65d-124">Header</span></span><br/> | <dl> <span data-ttu-id="9d65d-125"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d65d-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d65d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d65d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d65d-127">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="9d65d-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




