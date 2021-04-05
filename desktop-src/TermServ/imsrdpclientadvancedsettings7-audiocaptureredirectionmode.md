---
title: Propriedade IMsRdpClientAdvancedSettings7 AudioCaptureRedirectionMode
description: Especifica ou recupera um valor booliano que indica se o dispositivo de entrada de áudio padrão é redirecionado do cliente para a sessão remota.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AudioCaptureRedirectionMode
- Propriedade AudioCaptureRedirectionMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AudioCaptureRedirectionMode
- Propriedade AudioCaptureRedirectionMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918655"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="ebf86-108">Propriedade IMsRdpClientAdvancedSettings7:: AudioCaptureRedirectionMode</span><span class="sxs-lookup"><span data-stu-id="ebf86-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="ebf86-109">Especifica ou recupera um valor booliano que indica se o dispositivo de entrada de áudio padrão é redirecionado do cliente para a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="ebf86-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="ebf86-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ebf86-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf86-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf86-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="ebf86-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ebf86-112">Property value</span></span>

<span data-ttu-id="ebf86-113">Um **valor \_ bool de variante** que especifica se a captura de áudio é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ebf86-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="ebf86-114">Especifique **Variant \_ true** se desejar que a captura de áudio seja redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ebf86-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf86-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebf86-115">Requirements</span></span>



| <span data-ttu-id="ebf86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf86-116">Requirement</span></span> | <span data-ttu-id="ebf86-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf86-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf86-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf86-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebf86-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ebf86-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf86-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebf86-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ebf86-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ebf86-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebf86-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf86-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ebf86-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf86-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf86-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf86-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ebf86-126">IID</span><span class="sxs-lookup"><span data-stu-id="ebf86-126">IID</span></span><br/>                      | <span data-ttu-id="ebf86-127">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="ebf86-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf86-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebf86-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf86-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ebf86-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ebf86-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ebf86-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





