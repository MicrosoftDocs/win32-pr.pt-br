---
description: Aplica-se ao Windows Vista e posterior.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Propriedade AM_RATE_ResetOnTimeDisc (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792568"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="aba6e-103">Propriedade de ResetOnTimeDisc da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="aba6e-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="aba6e-104">Aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="aba6e-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="aba6e-105">Essa propriedade consulta se o decodificador ressincroniza os carimbos de hora de saída para os carimbos de hora de entrada quando o decodificador recebe um exemplo com o sinalizador de descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="aba6e-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="aba6e-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aba6e-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="aba6e-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="aba6e-107">Property Set GUID</span></span> | <span data-ttu-id="aba6e-108">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="aba6e-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="aba6e-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="aba6e-109">Property ID</span></span>       | <span data-ttu-id="aba6e-110">\_ResetOnTimeDisc de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="aba6e-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="aba6e-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="aba6e-111">Data Type</span></span>         | <span data-ttu-id="aba6e-112">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="aba6e-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="aba6e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aba6e-113">Remarks</span></span>

<span data-ttu-id="aba6e-114">Esta propriedade dá suporte a alterações de taxa suave.</span><span class="sxs-lookup"><span data-stu-id="aba6e-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="aba6e-115">Se o valor dessa propriedade for **true** e o decodificador receber um exemplo de entrada com o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, o quadro decodificado deverá ter o mesmo carimbo de data/hora que o quadro de entrada.</span><span class="sxs-lookup"><span data-stu-id="aba6e-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="aba6e-116">Para recuperar o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo.</span><span class="sxs-lookup"><span data-stu-id="aba6e-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="aba6e-117">O sinalizador é definido no membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="aba6e-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="aba6e-118">Para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="aba6e-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba6e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aba6e-119">Requirements</span></span>



| <span data-ttu-id="aba6e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aba6e-120">Requirement</span></span> | <span data-ttu-id="aba6e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="aba6e-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aba6e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aba6e-122">Header</span></span><br/> | <dl> <span data-ttu-id="aba6e-123"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba6e-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba6e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="aba6e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba6e-125">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="aba6e-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




