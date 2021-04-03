---
description: A \_ Propriedade PKEY AudioEngine \_ DeviceFormat especifica o formato de dispositivo, que é o formato que o usuário selecionou para o fluxo que flui entre o mecanismo de áudio e o dispositivo de ponto de extremidade de áudio quando o dispositivo opera no modo compartilhado.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646500"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="c8f11-103">PKEY \_ AudioEngine \_ DeviceFormat</span><span class="sxs-lookup"><span data-stu-id="c8f11-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="c8f11-104">A propriedade **PKEY \_ AudioEngine \_ DeviceFormat** especifica o formato de dispositivo, que é o formato que o usuário selecionou para o fluxo que flui entre o mecanismo de áudio e o dispositivo de ponto de extremidade de áudio quando o dispositivo opera no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c8f11-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="c8f11-105">Esse formato pode não ser o melhor formato padrão para o uso de um aplicativo de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c8f11-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="c8f11-106">Normalmente, um aplicativo de modo exclusivo encontra um formato de dispositivo adequado fazendo algumas chamadas para o método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="c8f11-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="c8f11-107">Para obter mais informações, consulte [formatos de dispositivo](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c8f11-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="c8f11-108">O membro **VT** da estrutura **PROPVARIANT** é definido como blob VT \_ .</span><span class="sxs-lookup"><span data-stu-id="c8f11-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="c8f11-109">O membro de **blob** da estrutura **PROPVARIANT** é uma estrutura do tipo **blob** que contém dois membros.</span><span class="sxs-lookup"><span data-stu-id="c8f11-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="c8f11-110">Member **BLOB. cbSize** é um **DWORD** que especifica o número de bytes na descrição do formato.</span><span class="sxs-lookup"><span data-stu-id="c8f11-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="c8f11-111">Member **BLOB. pBlobData** aponta para uma estrutura **WAVEFORMATEX** que contém a descrição do formato.</span><span class="sxs-lookup"><span data-stu-id="c8f11-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="c8f11-112">Para obter mais informações sobre **blob**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c8f11-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="c8f11-113">Para obter mais informações sobre o **WAVEFORMATEX**, consulte a documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="c8f11-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f11-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f11-114">Requirements</span></span>



| <span data-ttu-id="c8f11-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f11-115">Requirement</span></span> | <span data-ttu-id="c8f11-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c8f11-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f11-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8f11-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f11-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8f11-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c8f11-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8f11-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f11-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8f11-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c8f11-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8f11-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f11-122"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f11-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f11-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8f11-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f11-124">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="c8f11-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c8f11-125">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="c8f11-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




