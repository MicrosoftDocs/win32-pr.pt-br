---
description: Define o modo de processamento do MFT Estabilização de Vídeo.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Atributo MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090860"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="14a2b-103">\_Atributo de \_ modo VIDEODSP MF</span><span class="sxs-lookup"><span data-stu-id="14a2b-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="14a2b-104">Define o modo de processamento do [**MFT estabilização de vídeo**](video-stabilization-mft.md).</span><span class="sxs-lookup"><span data-stu-id="14a2b-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="14a2b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="14a2b-105">Data type</span></span>

<span data-ttu-id="14a2b-106">**MFVideoDSPMode** armazenado como **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="14a2b-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="14a2b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="14a2b-107">Remarks</span></span>

<span data-ttu-id="14a2b-108">O valor desse atributo é um valor de enumeração [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="14a2b-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="14a2b-109">Esse atributo pode ser usado para habilitar ou desabilitar a estabilização de imagem e pode ser atualizado para cada exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="14a2b-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="14a2b-110">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="14a2b-110">To set this attribute:</span></span>

1.  <span data-ttu-id="14a2b-111">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no MFT de estabilização de vídeo para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="14a2b-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="14a2b-112">Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para definir o atributo.</span><span class="sxs-lookup"><span data-stu-id="14a2b-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a2b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a2b-113">Requirements</span></span>



| <span data-ttu-id="14a2b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a2b-114">Requirement</span></span> | <span data-ttu-id="14a2b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="14a2b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14a2b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14a2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="14a2b-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="14a2b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="14a2b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14a2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="14a2b-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="14a2b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14a2b-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14a2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="14a2b-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a2b-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a2b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="14a2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a2b-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14a2b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="14a2b-124">**Estabilização de Vídeo MFT**</span><span class="sxs-lookup"><span data-stu-id="14a2b-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




