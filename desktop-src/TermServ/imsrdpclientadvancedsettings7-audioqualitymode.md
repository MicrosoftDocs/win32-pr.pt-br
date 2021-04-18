---
title: Propriedade IMsRdpClientAdvancedSettings7 AudioQualityMode
description: Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado. Por padrão, é definido como 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AudioQualityMode
- Propriedade AudioQualityMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AudioQualityMode
- Propriedade AudioQualityMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792597"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="3934c-109">Propriedade IMsRdpClientAdvancedSettings7:: AudioQualityMode</span><span class="sxs-lookup"><span data-stu-id="3934c-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="3934c-110">Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="3934c-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="3934c-111">Por padrão, é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="3934c-111">By default this is set to 0.</span></span>

<span data-ttu-id="3934c-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3934c-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3934c-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3934c-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="3934c-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3934c-114">Property value</span></span>

<span data-ttu-id="3934c-115">Um valor que especifica o modo de qualidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="3934c-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="3934c-116">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="3934c-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="3934c-117">0</span><span class="sxs-lookup"><span data-stu-id="3934c-117">0</span></span>
</dt> <dd>

<span data-ttu-id="3934c-118">Qualidade de áudio dinâmica.</span><span class="sxs-lookup"><span data-stu-id="3934c-118">Dynamic audio quality.</span></span> <span data-ttu-id="3934c-119">Essa é a configuração de qualidade de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="3934c-119">This is the default audio quality setting.</span></span> <span data-ttu-id="3934c-120">O servidor ajusta dinamicamente a qualidade de saída de áudio em resposta às condições de rede e aos recursos de cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="3934c-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="3934c-121">1</span><span class="sxs-lookup"><span data-stu-id="3934c-121">1</span></span>
</dt> <dd>

<span data-ttu-id="3934c-122">Qualidade de áudio médio.</span><span class="sxs-lookup"><span data-stu-id="3934c-122">Medium audio quality.</span></span> <span data-ttu-id="3934c-123">O servidor usa um formato fixo, mas compactado, para saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="3934c-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="3934c-124">2</span><span class="sxs-lookup"><span data-stu-id="3934c-124">2</span></span>
</dt> <dd>

<span data-ttu-id="3934c-125">Alta qualidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="3934c-125">High audio quality.</span></span> <span data-ttu-id="3934c-126">O servidor fornece a saída de áudio no formato PCM descompactado com menor sobrecarga de processamento para latência.</span><span class="sxs-lookup"><span data-stu-id="3934c-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3934c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3934c-127">Requirements</span></span>



| <span data-ttu-id="3934c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3934c-128">Requirement</span></span> | <span data-ttu-id="3934c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3934c-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3934c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3934c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3934c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3934c-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="3934c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3934c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3934c-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3934c-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="3934c-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3934c-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="3934c-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3934c-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3934c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3934c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3934c-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3934c-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3934c-138">IID</span><span class="sxs-lookup"><span data-stu-id="3934c-138">IID</span></span><br/>                      | <span data-ttu-id="3934c-139">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="3934c-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3934c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3934c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3934c-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3934c-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3934c-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3934c-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





