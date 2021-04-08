---
description: Desabilita a conversão de taxa de quadros na MFT do processador de vídeo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Atributo MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921123"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="fb893-103">MF \_ XVP \_ desabilitar o \_ atributo FRC</span><span class="sxs-lookup"><span data-stu-id="fb893-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="fb893-104">Desabilita a conversão de taxa de quadros na [**MFT do processador de vídeo**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="fb893-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="fb893-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fb893-105">Data type</span></span>

<span data-ttu-id="fb893-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="fb893-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fb893-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb893-107">Remarks</span></span>

<span data-ttu-id="fb893-108">Se esse atributo for **true**, o processador de vídeo não executará a conversão de taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="fb893-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="fb893-109">Por padrão, o processador de vídeo converterá a taxa de quadros para corresponder ao tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="fb893-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="fb893-110">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="fb893-110">To set this attribute:</span></span>

1.  <span data-ttu-id="fb893-111">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb893-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="fb893-112">Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fb893-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="fb893-113">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="fb893-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb893-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb893-114">Requirements</span></span>



| <span data-ttu-id="fb893-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb893-115">Requirement</span></span> | <span data-ttu-id="fb893-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fb893-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb893-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb893-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb893-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fb893-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb893-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb893-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb893-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fb893-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb893-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb893-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb893-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb893-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb893-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb893-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb893-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb893-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




