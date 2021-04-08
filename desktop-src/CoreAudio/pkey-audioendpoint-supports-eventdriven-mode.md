---
description: O PKEY \_ AudioEndpoint \_ dá suporte à \_ propriedade de modo EventDriven que \_ indica se o ponto de extremidade dá suporte ao modo controlado por evento.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920517"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="76947-103">PKEY \_ AudioEndpoint \_ dá suporte ao \_ \_ modo EventDriven</span><span class="sxs-lookup"><span data-stu-id="76947-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="76947-104">O **PKEY \_ AudioEndpoint \_ dá suporte à propriedade de \_ \_ modo EventDriven** que indica se o ponto de extremidade dá suporte ao modo controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="76947-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="76947-105">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="76947-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="76947-106">O membro **uintVal** da estrutura **PROPVARIANT** é um **DWORD** que indica se o ponto de extremidade dá suporte ao modo controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="76947-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="76947-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="76947-107">Remarks</span></span>

<span data-ttu-id="76947-108">Esse valor de propriedade é preenchido por um OEM de áudio em um arquivo. inf para indicar que o hardware HDAudio dá suporte ao modo controlado por eventos de acordo com o requisito do WHQL.</span><span class="sxs-lookup"><span data-stu-id="76947-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="76947-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76947-109">Requirements</span></span>



| <span data-ttu-id="76947-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="76947-110">Requirement</span></span> | <span data-ttu-id="76947-111">Valor</span><span class="sxs-lookup"><span data-stu-id="76947-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76947-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76947-112">Minimum supported client</span></span><br/> | <span data-ttu-id="76947-113">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76947-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="76947-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76947-114">Minimum supported server</span></span><br/> | <span data-ttu-id="76947-115">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="76947-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76947-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76947-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="76947-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76947-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76947-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="76947-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76947-119">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="76947-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="76947-120">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="76947-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




