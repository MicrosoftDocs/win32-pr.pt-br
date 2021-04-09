---
description: A \_ Propriedade PKEY AudioEngine \_ OEMFormat especifica o formato padrão do dispositivo que é usado para renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089510"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="d478d-104">PKEY \_ AudioEngine \_ OEMFormat</span><span class="sxs-lookup"><span data-stu-id="d478d-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="d478d-105">A \_ Propriedade PKEY AudioEngine \_ OEMFormat especifica o formato padrão do dispositivo que é usado para renderizar ou capturar um fluxo.</span><span class="sxs-lookup"><span data-stu-id="d478d-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="d478d-106">Os valores são preenchidos pelo OEM em um arquivo. inf.</span><span class="sxs-lookup"><span data-stu-id="d478d-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="d478d-107">O membro **VT** da estrutura **PROPVARIANT** é definido como blob VT \_ .</span><span class="sxs-lookup"><span data-stu-id="d478d-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="d478d-108">O membro de **blob** da estrutura **PROPVARIANT** é uma estrutura do tipo **blob** que contém dois membros.</span><span class="sxs-lookup"><span data-stu-id="d478d-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="d478d-109">Member **BLOB. cbSize** é um **DWORD** que especifica o número de bytes na descrição do formato.</span><span class="sxs-lookup"><span data-stu-id="d478d-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="d478d-110">Member **BLOB. pBlobData** aponta para uma estrutura **WAVEFORMATEX** que contém a descrição do formato.</span><span class="sxs-lookup"><span data-stu-id="d478d-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="d478d-111">Para obter mais informações sobre BLOB, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d478d-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="d478d-112">Para obter mais informações sobre o **WAVEFORMATEX**, consulte a documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="d478d-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d478d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d478d-113">Requirements</span></span>



| <span data-ttu-id="d478d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d478d-114">Requirement</span></span> | <span data-ttu-id="d478d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d478d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d478d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d478d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d478d-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d478d-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d478d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d478d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d478d-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d478d-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d478d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d478d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d478d-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d478d-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d478d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d478d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d478d-123">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="d478d-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="d478d-124">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="d478d-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




