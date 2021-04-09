---
description: Especifica o número máximo de amostras de saída que uma Microsoft Media Foundation transformação (MFT) terá pendente no pipeline a qualquer momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Atributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164761"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="c3dbc-103">\_Atributo de \_ \_ contagem de amostras de saída mínima \_ \_ de</span><span class="sxs-lookup"><span data-stu-id="c3dbc-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="c3dbc-104">Especifica o número máximo de amostras de saída que uma Microsoft Media Foundation transformação (MFT) terá pendente no pipeline a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="c3dbc-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3dbc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c3dbc-105">Data type</span></span>

<span data-ttu-id="c3dbc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3dbc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3dbc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3dbc-107">Remarks</span></span>

<span data-ttu-id="c3dbc-108">Esse atributo aplica-se somente a MFTs que usam um buffer circular para alocar seus próprios exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="c3dbc-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="c3dbc-109">Outros MFTs ignoram esse atributo.</span><span class="sxs-lookup"><span data-stu-id="c3dbc-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="c3dbc-110">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="c3dbc-110">To set this attribute:</span></span>

1.  <span data-ttu-id="c3dbc-111">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c3dbc-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="c3dbc-112">Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.</span><span class="sxs-lookup"><span data-stu-id="c3dbc-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3dbc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3dbc-113">Requirements</span></span>



| <span data-ttu-id="c3dbc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3dbc-114">Requirement</span></span> | <span data-ttu-id="c3dbc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c3dbc-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dbc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3dbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3dbc-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c3dbc-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c3dbc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3dbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3dbc-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c3dbc-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c3dbc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3dbc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3dbc-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3dbc-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3dbc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3dbc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3dbc-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3dbc-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3dbc-124">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="c3dbc-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




