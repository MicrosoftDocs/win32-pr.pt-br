---
description: Permite que o processador de vídeo avançado (EVR) chame em lote o método Microsoft Direct3D IDirect3DDevice9::P reenviado.
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: Atributo EVRConfig_AllowBatching (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191c3c0f0ea4ad18e7bb711ae6d37c21f75cd478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501169"
---
# <a name="evrconfig_allowbatching-attribute"></a><span data-ttu-id="b1f26-103">\_Atributo EVRConfig AllowBatching</span><span class="sxs-lookup"><span data-stu-id="b1f26-103">EVRConfig\_AllowBatching attribute</span></span>

<span data-ttu-id="b1f26-104">Permite que o processador de vídeo avançado (EVR) chame em lote o método Microsoft Direct3D **IDirect3DDevice9::P reenviado** .</span><span class="sxs-lookup"><span data-stu-id="b1f26-104">Allows the Enhanced Video Renderer (EVR) to batch calls to the Microsoft Direct3D **IDirect3DDevice9::Present** method.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1f26-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b1f26-105">Data type</span></span>

<span data-ttu-id="b1f26-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1f26-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b1f26-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b1f26-107">Get/set</span></span>

<span data-ttu-id="b1f26-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b1f26-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b1f26-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b1f26-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f26-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1f26-110">Remarks</span></span>

<span data-ttu-id="b1f26-111">Esse atributo pode ser definido no coletor de mídia do EVR.</span><span class="sxs-lookup"><span data-stu-id="b1f26-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="b1f26-112">Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="b1f26-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="b1f26-113">Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoRenderPrefs \_ ALLOWBATCHING** no EVR.</span><span class="sxs-lookup"><span data-stu-id="b1f26-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowBatching** flag on the EVR.</span></span> <span data-ttu-id="b1f26-114">Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obter uma descrição desse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="b1f26-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="b1f26-115">A constante de GUID para esse atributo é exportada de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="b1f26-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f26-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f26-116">Requirements</span></span>



| <span data-ttu-id="b1f26-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f26-117">Requirement</span></span> | <span data-ttu-id="b1f26-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f26-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f26-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f26-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f26-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1f26-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b1f26-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f26-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f26-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b1f26-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b1f26-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1f26-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f26-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f26-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1f26-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1f26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f26-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1f26-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1f26-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="b1f26-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1f26-128">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="b1f26-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




