---
description: Permite que o processador de vídeo avançado (EVR) limite sua saída para corresponder à largura de banda da GPU.
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: Atributo EVRConfig_AllowDropToThrottle (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97cbab6fae6644b3c0187d09edb59ab2538012e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010308"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a><span data-ttu-id="38191-103">\_Atributo EVRConfig AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="38191-103">EVRConfig\_AllowDropToThrottle attribute</span></span>

<span data-ttu-id="38191-104">Permite que o processador de vídeo avançado (EVR) limite sua saída para corresponder à largura de banda da GPU.</span><span class="sxs-lookup"><span data-stu-id="38191-104">Allows the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="38191-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="38191-105">Data type</span></span>

<span data-ttu-id="38191-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="38191-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="38191-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="38191-107">Get/set</span></span>

<span data-ttu-id="38191-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="38191-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="38191-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="38191-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="38191-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="38191-110">Remarks</span></span>

<span data-ttu-id="38191-111">Esse atributo pode ser definido no coletor de mídia do EVR.</span><span class="sxs-lookup"><span data-stu-id="38191-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="38191-112">Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="38191-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="38191-113">Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoRenderPrefs \_ ALLOWOUTPUTTHROTTLING** no EVR.</span><span class="sxs-lookup"><span data-stu-id="38191-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="38191-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obter uma descrição desse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="38191-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="38191-115">A constante de GUID para esse atributo é exportada de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="38191-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="38191-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38191-116">Requirements</span></span>



| <span data-ttu-id="38191-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38191-117">Requirement</span></span> | <span data-ttu-id="38191-118">Valor</span><span class="sxs-lookup"><span data-stu-id="38191-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38191-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38191-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38191-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="38191-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38191-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38191-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38191-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="38191-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="38191-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38191-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="38191-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="38191-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38191-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="38191-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38191-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="38191-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="38191-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="38191-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="38191-128">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="38191-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




