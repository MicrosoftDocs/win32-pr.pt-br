---
description: Força o processador de vídeo avançado (EVR) a misturar o vídeo em um retângulo menor do que o retângulo de saída e, em seguida, dimensionar o resultado.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: Atributo EVRConfig_ForceScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82b7e017d414e86b8b4332fe5646e4808d4009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010307"
---
# <a name="evrconfig_forcescaling-attribute"></a><span data-ttu-id="a6738-103">\_Atributo EVRConfig ForceScaling</span><span class="sxs-lookup"><span data-stu-id="a6738-103">EVRConfig\_ForceScaling attribute</span></span>

<span data-ttu-id="a6738-104">Força o processador de vídeo avançado (EVR) a misturar o vídeo em um retângulo menor do que o retângulo de saída e, em seguida, dimensionar o resultado.</span><span class="sxs-lookup"><span data-stu-id="a6738-104">Forces the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6738-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a6738-105">Data type</span></span>

<span data-ttu-id="a6738-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6738-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a6738-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="a6738-107">Get/set</span></span>

<span data-ttu-id="a6738-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a6738-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a6738-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a6738-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6738-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6738-110">Remarks</span></span>

<span data-ttu-id="a6738-111">Esse atributo pode ser definido no coletor de mídia do EVR.</span><span class="sxs-lookup"><span data-stu-id="a6738-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="a6738-112">Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="a6738-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="a6738-113">Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoRenderPrefs \_ FORCESCALING** no EVR.</span><span class="sxs-lookup"><span data-stu-id="a6738-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceScaling** flag on the EVR.</span></span> <span data-ttu-id="a6738-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obter uma descrição desse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a6738-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="a6738-115">A constante de GUID para esse atributo é exportada de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="a6738-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6738-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6738-116">Requirements</span></span>



| <span data-ttu-id="a6738-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6738-117">Requirement</span></span> | <span data-ttu-id="a6738-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a6738-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6738-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6738-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6738-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a6738-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a6738-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6738-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6738-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a6738-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a6738-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6738-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6738-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6738-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6738-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6738-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6738-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6738-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6738-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="a6738-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6738-128">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="a6738-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




