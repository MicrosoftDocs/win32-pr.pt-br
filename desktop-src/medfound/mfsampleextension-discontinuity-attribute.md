---
description: Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: Atributo MFSampleExtension_Discontinuity (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502286"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="f102c-103">\_Atributo de descontinuidade MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="f102c-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="f102c-104">Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.</span><span class="sxs-lookup"><span data-stu-id="f102c-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="f102c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f102c-105">Data type</span></span>

<span data-ttu-id="f102c-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f102c-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f102c-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="f102c-107">Get/set</span></span>

<span data-ttu-id="f102c-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f102c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f102c-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f102c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f102c-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="f102c-110">Applies to</span></span>

[<span data-ttu-id="f102c-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f102c-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="f102c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f102c-112">Remarks</span></span>

<span data-ttu-id="f102c-113">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="f102c-113">This attribute applies to media samples.</span></span> <span data-ttu-id="f102c-114">Se esse atributo for **true**, significa que houve uma descontinuidade no fluxo e esse exemplo é o primeiro a aparecer após a lacuna.</span><span class="sxs-lookup"><span data-stu-id="f102c-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="f102c-115">Se esse atributo não for definido, o valor padrão será **false**.</span><span class="sxs-lookup"><span data-stu-id="f102c-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="f102c-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f102c-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f102c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f102c-117">Requirements</span></span>



| <span data-ttu-id="f102c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f102c-118">Requirement</span></span> | <span data-ttu-id="f102c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f102c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f102c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f102c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f102c-121">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="f102c-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f102c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f102c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f102c-123">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f102c-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f102c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f102c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f102c-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f102c-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f102c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f102c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f102c-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f102c-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f102c-128">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="f102c-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="f102c-129">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="f102c-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




