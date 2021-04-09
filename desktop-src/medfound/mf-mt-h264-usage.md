---
description: Especifica o modo de uso para um codificador UVC H. 264.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: Atributo MF_MT_H264_USAGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090572"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="0e859-103">\_Atributo de \_ uso de H264 do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="0e859-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="0e859-104">Especifica o modo de uso para um codificador UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="0e859-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e859-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e859-105">Data type</span></span>

<span data-ttu-id="0e859-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0e859-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0e859-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0e859-107">Get/set</span></span>

<span data-ttu-id="0e859-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0e859-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0e859-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0e859-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0e859-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="0e859-110">Applies to</span></span>

[<span data-ttu-id="0e859-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0e859-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="0e859-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e859-112">Remarks</span></span>

<span data-ttu-id="0e859-113">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="0e859-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="0e859-114">O valor corresponde ao campo **bUsage** no controle de teste/confirmação UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="0e859-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e859-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e859-115">Requirements</span></span>



| <span data-ttu-id="0e859-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e859-116">Requirement</span></span> | <span data-ttu-id="0e859-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0e859-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e859-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e859-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e859-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e859-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0e859-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e859-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e859-121">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e859-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0e859-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e859-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e859-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e859-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e859-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e859-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e859-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e859-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e859-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="0e859-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




