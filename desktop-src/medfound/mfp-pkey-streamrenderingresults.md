---
description: Especifica quais fluxos foram conectados com êxito a um coletor de mídia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Propriedade MFP_PKEY_StreamRenderingResults (Mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296434"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="1be14-103">\_Propriedade PKEY \_ STREAMRENDERINGRESULTS de MFP</span><span class="sxs-lookup"><span data-stu-id="1be14-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1be14-104">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1be14-104">Deprecated.</span></span> <span data-ttu-id="1be14-105">Essa API pode ser removida de versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="1be14-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="1be14-106">Os aplicativos devem usar a [sessão de mídia](media-session.md) para reprodução.</span><span class="sxs-lookup"><span data-stu-id="1be14-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="1be14-107">Especifica quais fluxos foram conectados com êxito a um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="1be14-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="1be14-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1be14-108">Data type</span></span>

<span data-ttu-id="1be14-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1be14-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1be14-110">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1be14-110">PROPVARIANT member</span></span>

<span data-ttu-id="1be14-111">Matriz de valores **DWORD** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="1be14-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="1be14-112">\_UI4 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="1be14-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="1be14-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="1be14-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="1be14-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be14-114">Remarks</span></span>

<span data-ttu-id="1be14-115">Essa propriedade pode ser enviada com o **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** Event.</span><span class="sxs-lookup"><span data-stu-id="1be14-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="1be14-116">O valor da propriedade é uma matriz de **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="1be14-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="1be14-117">As entradas de matriz correspondem aos fluxos no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="1be14-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="1be14-118">Cada entrada na matriz indica se o fluxo correspondente foi conectado a um coletor de mídia, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1be14-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="1be14-119">Se o fluxo estiver conectado a um coletor de mídia, o valor será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1be14-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="1be14-120">Se o fluxo não estiver selecionado, o valor será **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="1be14-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="1be14-121">Se um erro ocorreu ao tentar conectar o fluxo, o valor é um código de erro.</span><span class="sxs-lookup"><span data-stu-id="1be14-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="1be14-122">Se pelo menos um fluxo foi conectado com êxito, a reprodução é possível.</span><span class="sxs-lookup"><span data-stu-id="1be14-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="1be14-123">Por exemplo, o usuário pode ter o codec necessário para reproduzir o fluxo de áudio, mas não para reproduzir o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1be14-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be14-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1be14-124">Requirements</span></span>



| <span data-ttu-id="1be14-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be14-125">Requirement</span></span> | <span data-ttu-id="1be14-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1be14-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1be14-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1be14-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1be14-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1be14-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1be14-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="1be14-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1be14-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1be14-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be14-132"><dt>Mfplay. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be14-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be14-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be14-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be14-134">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1be14-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1be14-135">**\_MEDIAITEM de \_ conjunto de \_ eventos da MFP**</span><span class="sxs-lookup"><span data-stu-id="1be14-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




