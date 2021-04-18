---
title: Propriedade IMsRdpClientAdvancedSettings7 VideoPlaybackMode
description: Especifica ou recupera um valor que indica o modo de reprodução de vídeo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade VideoPlaybackMode
- Propriedade VideoPlaybackMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade VideoPlaybackMode
- Propriedade VideoPlaybackMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369930"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="ae9ab-108">Propriedade IMsRdpClientAdvancedSettings7:: VideoPlaybackMode</span><span class="sxs-lookup"><span data-stu-id="ae9ab-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="ae9ab-109">Especifica ou recupera um valor que indica o modo de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="ae9ab-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9ab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae9ab-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="ae9ab-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ae9ab-112">Property value</span></span>

<span data-ttu-id="ae9ab-113">Um valor que especifica o modo de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="ae9ab-114">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="ae9ab-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="ae9ab-115">1</span><span class="sxs-lookup"><span data-stu-id="ae9ab-115">1</span></span>
</dt> <dd>

<span data-ttu-id="ae9ab-116">O modo de reprodução de vídeo padrão.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-116">The default video playback mode.</span></span> <span data-ttu-id="ae9ab-117">Quando o modo de reprodução de vídeo é definido com esse valor, o redirecionamento de vídeo é controlado pela propriedade [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) .</span><span class="sxs-lookup"><span data-stu-id="ae9ab-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="ae9ab-118">Quando a propriedade **AudioRedirectionMode** é definida como **\_ \_ redirecionamento do modo de áudio**, o vídeo é decodificado e renderizado no cliente.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="ae9ab-119">0</span><span class="sxs-lookup"><span data-stu-id="ae9ab-119">0</span></span>
</dt> <dd>

<span data-ttu-id="ae9ab-120">O redirecionamento de reprodução de vídeo está desabilitado, mesmo quando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) está definido como **\_ \_ redirecionamento do modo de áudio**.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="ae9ab-121">Nesse modo, o vídeo é decodificado e renderizado no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="ae9ab-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae9ab-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae9ab-122">Requirements</span></span>



| <span data-ttu-id="ae9ab-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae9ab-123">Requirement</span></span> | <span data-ttu-id="ae9ab-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ae9ab-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9ab-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae9ab-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9ab-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae9ab-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ae9ab-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae9ab-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9ab-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae9ab-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ae9ab-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ae9ab-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae9ab-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ab-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ae9ab-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9ab-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9ab-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ab-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ae9ab-133">IID</span><span class="sxs-lookup"><span data-stu-id="ae9ab-133">IID</span></span><br/>                      | <span data-ttu-id="ae9ab-134">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="ae9ab-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae9ab-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae9ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9ab-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ae9ab-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ae9ab-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ae9ab-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





