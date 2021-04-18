---
description: Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo. Este é um alias do \_ nível MF MT do \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Atributo MF_MT_VIDEO_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785252"
---
# <a name="mf_mt_video_level-attribute"></a><span data-ttu-id="41b32-104">\_Atributo de \_ nível de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="41b32-104">MF\_MT\_VIDEO\_LEVEL attribute</span></span>

<span data-ttu-id="41b32-105">Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41b32-105">Specifies the MPEG-2 or H.264 level in a video media type.</span></span> <span data-ttu-id="41b32-106">Este é um alias do [ \_ \_ \_ nível MF MT do MPEG2](mf-mt-mpeg2-level-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="41b32-106">This is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="41b32-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="41b32-107">Data type</span></span>

<span data-ttu-id="41b32-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="41b32-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="41b32-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="41b32-109">Remarks</span></span>

<span data-ttu-id="41b32-110">**Codificadores H. 264:**</span><span class="sxs-lookup"><span data-stu-id="41b32-110">**H.264 encoders:**</span></span>

<span data-ttu-id="41b32-111">Os níveis com suporte são estendidos para incluir o [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span><span class="sxs-lookup"><span data-stu-id="41b32-111">Supported levels are extended to include the [**eAVEncH264VLevel5\_2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span></span>

<span data-ttu-id="41b32-112">Padrão: o padrão recomendado é selecionar o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo a resolução, a taxa de quadros etc.</span><span class="sxs-lookup"><span data-stu-id="41b32-112">Default : Recommended default is to select the minimum level to match video encoding configuration including resolution, frame rate etc.</span></span>

<span data-ttu-id="41b32-113">Padrão recomendado: selecione o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo a resolução, a taxa de quadros, etc.</span><span class="sxs-lookup"><span data-stu-id="41b32-113">Recommended default: select the minimum level to match video encoding configuration including resolution, frame rate, etc.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b32-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41b32-114">Requirements</span></span>



| <span data-ttu-id="41b32-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b32-115">Requirement</span></span> | <span data-ttu-id="41b32-116">Valor</span><span class="sxs-lookup"><span data-stu-id="41b32-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41b32-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41b32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41b32-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41b32-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="41b32-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41b32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41b32-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="41b32-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="41b32-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41b32-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b32-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41b32-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b32-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="41b32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b32-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41b32-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




