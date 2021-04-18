---
description: Define o número máximo de iterações de pesquisa que a fonte de mídia do ASF usará quando executar a busca iterativa.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763914"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="cdc60-103">\_Propriedade de \_ \_ contagem máxima \_ de MFPKEY ASFMediaSource IterativeSeek</span><span class="sxs-lookup"><span data-stu-id="cdc60-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="cdc60-104">Define o número máximo de iterações de pesquisa que a fonte de mídia do ASF usará quando executar a busca iterativa.</span><span class="sxs-lookup"><span data-stu-id="cdc60-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="cdc60-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cdc60-105">Data type</span></span>

<span data-ttu-id="cdc60-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="cdc60-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="cdc60-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="cdc60-107">PROPVARIANT member</span></span>

<span data-ttu-id="cdc60-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="cdc60-108">**ULONG**</span></span>

<span data-ttu-id="cdc60-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="cdc60-109">VT\_UI4</span></span>

<span data-ttu-id="cdc60-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="cdc60-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="cdc60-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdc60-111">Remarks</span></span>

<span data-ttu-id="cdc60-112">Use essa propriedade para configurar a origem da mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="cdc60-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="cdc60-113">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="cdc60-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="cdc60-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="cdc60-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="cdc60-115">Essa propriedade só se aplica quando a busca iterativa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cdc60-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="cdc60-116">Para obter mais informações, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="cdc60-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="cdc60-117">O intervalo válido dessa propriedade é \[ 1-10 \] , inclusive.</span><span class="sxs-lookup"><span data-stu-id="cdc60-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="cdc60-118">Com um número mais alto, a busca iterativa tende a ser mais precisa, mas leva mais tempo.</span><span class="sxs-lookup"><span data-stu-id="cdc60-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="cdc60-119">O valor padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="cdc60-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc60-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdc60-120">Requirements</span></span>



| <span data-ttu-id="cdc60-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc60-121">Requirement</span></span> | <span data-ttu-id="cdc60-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cdc60-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc60-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdc60-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc60-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cdc60-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cdc60-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdc60-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc60-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="cdc60-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cdc60-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdc60-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc60-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc60-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc60-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdc60-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc60-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdc60-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




