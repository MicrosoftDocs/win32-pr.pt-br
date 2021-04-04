---
title: Objeto de transcriptografador DRM
description: Objeto de transcriptografador DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- SDK do Windows Media Format, objetos de criptografia DRM
- ASF (Advanced Systems Format), objetos de criptografia de DRM
- ASF (formato de sistemas avançados), objetos de criptografia de DRM
- objetos, objetos de criptografador DRM
- Objetos do transcriptografador DRM
- SDK do Windows Media Format, objetos de criptografia
- Formato de sistema avançado (ASF), objetos transcriptr
- ASF (formato de sistemas avançados), objetos de criptografia
- objetos, objetos transcriptr
- objetos transcriptr
- DRM (gerenciamento de direitos digitais), objetos de criptografia
- DRM (gerenciamento de direitos digitais), objetos de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084358"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="a0d12-115">Objeto de transcriptografador DRM</span><span class="sxs-lookup"><span data-stu-id="a0d12-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="a0d12-116">O objeto de criptografador DRM converte arquivos ASF protegidos por DRM em fluxos de dados prontos para serem enviados a dispositivos de rede que usam o Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="a0d12-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="a0d12-117">O objeto de criptografador DRM é criado pela função [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) , que define um ponteiro para a interface [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .</span><span class="sxs-lookup"><span data-stu-id="a0d12-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="a0d12-118">**IUnknown** e **IWMDRMTranscryptor** são as únicas interfaces suportadas por este objeto.</span><span class="sxs-lookup"><span data-stu-id="a0d12-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0d12-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0d12-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d12-120">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="a0d12-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




