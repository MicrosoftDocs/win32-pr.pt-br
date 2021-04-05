---
description: Especifica como uma Media Foundation transformação (MFT) deve gerar um fluxo de vídeo 3D estereoscópico.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Atributo MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827625"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="19ca3-103">\_Atributo de saída MF Enable \_ 3DVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="19ca3-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="19ca3-104">Especifica como uma Media Foundation transformação (MFT) deve gerar um fluxo de vídeo 3D estereoscópico.</span><span class="sxs-lookup"><span data-stu-id="19ca3-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="19ca3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19ca3-105">Data type</span></span>

<span data-ttu-id="19ca3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19ca3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19ca3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="19ca3-107">Remarks</span></span>

<span data-ttu-id="19ca3-108">O valor do atributo é um membro da enumeração [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .</span><span class="sxs-lookup"><span data-stu-id="19ca3-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="19ca3-109">Esse atributo se aplica somente se o MFT retornar **true** para o atributo [ \_ \_ 3DVIDEO de suporte do MFT](mft-support-3dvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="19ca3-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="19ca3-110">Para obter ou definir este atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global do MFT.</span><span class="sxs-lookup"><span data-stu-id="19ca3-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ca3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ca3-111">Requirements</span></span>



| <span data-ttu-id="19ca3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ca3-112">Requirement</span></span> | <span data-ttu-id="19ca3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="19ca3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19ca3-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19ca3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="19ca3-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19ca3-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="19ca3-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19ca3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="19ca3-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19ca3-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="19ca3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19ca3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ca3-119"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ca3-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ca3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="19ca3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ca3-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19ca3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




