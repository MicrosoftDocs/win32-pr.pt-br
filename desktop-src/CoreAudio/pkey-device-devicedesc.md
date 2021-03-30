---
description: A propriedade PKEY do \_ dispositivo \_ DeviceDesc contém a descrição do dispositivo do ponto de extremidade (por exemplo, &\# 0034; Alto-falantes&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826102"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="ff46a-103">PKEY \_ dispositivo \_ DeviceDesc</span><span class="sxs-lookup"><span data-stu-id="ff46a-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="ff46a-104">A propriedade **PKEY do \_ dispositivo \_ DeviceDesc** contém a descrição do dispositivo do ponto de extremidade (por exemplo, "alto-falantes").</span><span class="sxs-lookup"><span data-stu-id="ff46a-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="ff46a-105">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="ff46a-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="ff46a-106">O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém a descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff46a-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff46a-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff46a-107">Requirements</span></span>



| <span data-ttu-id="ff46a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff46a-108">Requirement</span></span> | <span data-ttu-id="ff46a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="ff46a-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff46a-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff46a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ff46a-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff46a-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff46a-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff46a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ff46a-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff46a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ff46a-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff46a-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff46a-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff46a-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff46a-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ff46a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff46a-117">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="ff46a-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="ff46a-118">Propriedades do Dispositivo</span><span class="sxs-lookup"><span data-stu-id="ff46a-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




