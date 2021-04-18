---
description: Define a tolerância, em milissegundos, que é usada quando a origem de mídia do ASF executa a busca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810760"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="4cece-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerância \_ na \_ propriedade de milissegundos</span><span class="sxs-lookup"><span data-stu-id="4cece-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="4cece-104">Define a tolerância, em milissegundos, que é usada quando a origem de mídia do ASF executa a busca iterativa.</span><span class="sxs-lookup"><span data-stu-id="4cece-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="4cece-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4cece-105">Data type</span></span>

<span data-ttu-id="4cece-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="4cece-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4cece-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4cece-107">PROPVARIANT member</span></span>

<span data-ttu-id="4cece-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="4cece-108">**ULONG**</span></span>

<span data-ttu-id="4cece-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="4cece-109">VT\_UI4</span></span>

<span data-ttu-id="4cece-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="4cece-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4cece-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cece-111">Remarks</span></span>

<span data-ttu-id="4cece-112">Use essa propriedade para configurar a origem da mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="4cece-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="4cece-113">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="4cece-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="4cece-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="4cece-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="4cece-115">Essa propriedade só se aplica quando a busca iterativa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4cece-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="4cece-116">Para obter mais informações, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="4cece-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="4cece-117">O algoritmo de busca interativa é interrompido se encontrar um pacote cuja distância do tempo de busca está dentro da tolerância especificada.</span><span class="sxs-lookup"><span data-stu-id="4cece-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="4cece-118">O valor padrão é 8000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="4cece-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cece-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cece-119">Requirements</span></span>



| <span data-ttu-id="4cece-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cece-120">Requirement</span></span> | <span data-ttu-id="4cece-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4cece-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cece-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cece-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cece-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4cece-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4cece-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cece-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cece-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4cece-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4cece-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cece-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cece-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cece-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cece-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cece-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cece-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4cece-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




