---
description: Identificador para a janela de recorte de vídeo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Atributo MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789922"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="52ffa-103">\_Atributo da \_ janela ativar vídeo do MF \_</span><span class="sxs-lookup"><span data-stu-id="52ffa-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="52ffa-104">Identificador para a janela de recorte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="52ffa-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="52ffa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="52ffa-105">Data type</span></span>

<span data-ttu-id="52ffa-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="52ffa-106">**UINT64**</span></span>

<span data-ttu-id="52ffa-107">Tratar como **DWORD \_ PTR** (**hWnd**).</span><span class="sxs-lookup"><span data-stu-id="52ffa-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="52ffa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="52ffa-108">Remarks</span></span>

<span data-ttu-id="52ffa-109">Esse atributo se aplica ao objeto de ativação para o processador de vídeo avançado (EVR).</span><span class="sxs-lookup"><span data-stu-id="52ffa-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="52ffa-110">O valor é definido automaticamente quando você chama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar o objeto de ativação EVR.</span><span class="sxs-lookup"><span data-stu-id="52ffa-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="52ffa-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="52ffa-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ffa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ffa-112">Requirements</span></span>



| <span data-ttu-id="52ffa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ffa-113">Requirement</span></span> | <span data-ttu-id="52ffa-114">Valor</span><span class="sxs-lookup"><span data-stu-id="52ffa-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52ffa-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ffa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="52ffa-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52ffa-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="52ffa-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ffa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="52ffa-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52ffa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="52ffa-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52ffa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ffa-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ffa-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ffa-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="52ffa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ffa-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52ffa-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52ffa-123">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="52ffa-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="52ffa-124">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="52ffa-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="52ffa-125">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="52ffa-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="52ffa-126">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="52ffa-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




