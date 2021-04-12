---
description: Indica o número mínimo de amostras progressivas que a Microsoft Media Foundation transformação (MFT) deve permitir que seja pendentes em um determinado momento.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Atributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170365"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="4e7f3-103">\_ \_ \_ \_ \_ Atributo progressivo da contagem de amostras de saída mínima \_ de MF</span><span class="sxs-lookup"><span data-stu-id="4e7f3-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="4e7f3-104">Indica o número mínimo de amostras progressivas que a Microsoft Media Foundation transformação (MFT) deve permitir que seja pendentes em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="4e7f3-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e7f3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4e7f3-105">Data type</span></span>

<span data-ttu-id="4e7f3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4e7f3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7f3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e7f3-107">Remarks</span></span>

<span data-ttu-id="4e7f3-108">Esse atributo aplica-se somente a MFTs que usam um buffer circular para alocar seus próprios exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="4e7f3-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="4e7f3-109">Outros MFTs ignoram esse atributo.</span><span class="sxs-lookup"><span data-stu-id="4e7f3-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="4e7f3-110">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="4e7f3-110">To set this attribute:</span></span>

1.  <span data-ttu-id="4e7f3-111">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4e7f3-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="4e7f3-112">Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.</span><span class="sxs-lookup"><span data-stu-id="4e7f3-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7f3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e7f3-113">Requirements</span></span>



| <span data-ttu-id="4e7f3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7f3-114">Requirement</span></span> | <span data-ttu-id="4e7f3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4e7f3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7f3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e7f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e7f3-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e7f3-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4e7f3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e7f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e7f3-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e7f3-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4e7f3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e7f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e7f3-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e7f3-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7f3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e7f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7f3-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e7f3-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




