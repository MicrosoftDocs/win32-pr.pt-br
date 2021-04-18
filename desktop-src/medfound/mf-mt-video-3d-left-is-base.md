---
description: Para um formato de vídeo 3D, especifica qual exibição é a exibição de base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Atributo MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785323"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="6f70f-103">A \_ esquerda do vídeo MF MT \_ \_ 3D \_ é o \_ \_ atributo base</span><span class="sxs-lookup"><span data-stu-id="6f70f-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="6f70f-104">Para um formato de vídeo 3D, especifica qual exibição é a exibição de base.</span><span class="sxs-lookup"><span data-stu-id="6f70f-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f70f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6f70f-105">Data type</span></span>

<span data-ttu-id="6f70f-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="6f70f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f70f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f70f-107">Remarks</span></span>

<span data-ttu-id="6f70f-108">Por padrão, a exibição à esquerda em uma sequência de vídeo 3D é a exibição de base.</span><span class="sxs-lookup"><span data-stu-id="6f70f-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="6f70f-109">Se o modo de exibição à direita for o modo de exibição de base, defina esse atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="6f70f-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="6f70f-110">Para converter o vídeo estereoscópico em 2D, mantenha o modo de exibição de base e descarte o outro modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6f70f-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f70f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f70f-111">Requirements</span></span>



| <span data-ttu-id="6f70f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f70f-112">Requirement</span></span> | <span data-ttu-id="6f70f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6f70f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f70f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f70f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6f70f-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f70f-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6f70f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f70f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6f70f-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f70f-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6f70f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f70f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f70f-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f70f-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f70f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f70f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f70f-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f70f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




