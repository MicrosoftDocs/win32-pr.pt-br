---
description: Define um Visual DirectComposition da Microsoft como a região de reprodução para o mecanismo de mídia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Atributo MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105752326"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="276d5-103">\_ \_ \_ Atributo Visual de reprodução do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="276d5-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="276d5-104">Define um Visual DirectComposition da Microsoft como a região de reprodução para o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="276d5-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="276d5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="276d5-105">Data type</span></span>

<span data-ttu-id="276d5-106">**IDCompositionVisual \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="276d5-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="276d5-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="276d5-107">Get/set</span></span>

<span data-ttu-id="276d5-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="276d5-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="276d5-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="276d5-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="276d5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="276d5-110">Remarks</span></span>

<span data-ttu-id="276d5-111">Para obter mais informações sobre DirectComposition, consulte [DirectComposition](../directcomp/directcomposition-portal.md) e [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="276d5-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="276d5-112">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="276d5-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="276d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="276d5-113">Requirements</span></span>



| <span data-ttu-id="276d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="276d5-114">Requirement</span></span> | <span data-ttu-id="276d5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="276d5-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="276d5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="276d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="276d5-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="276d5-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="276d5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="276d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="276d5-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="276d5-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="276d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="276d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="276d5-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="276d5-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="276d5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="276d5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276d5-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="276d5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
