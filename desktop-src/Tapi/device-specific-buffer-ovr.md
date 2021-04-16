---
description: Os buffers específicos do dispositivo podem fazer parte de uma implementação de provedores de serviço de operações estendidas. O provedor de serviços define o significado desses buffers.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Buffer específico do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779470"
---
# <a name="device-specific-buffer"></a><span data-ttu-id="41526-104">Buffer específico do dispositivo</span><span class="sxs-lookup"><span data-stu-id="41526-104">Device-specific Buffer</span></span>

<span data-ttu-id="41526-105">Os buffers específicos do dispositivo podem fazer parte da implementação de operações estendidas de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="41526-105">Device-specific buffers may be part of a service provider's implementation of extended operations.</span></span> <span data-ttu-id="41526-106">O provedor de serviços define o significado desses buffers.</span><span class="sxs-lookup"><span data-stu-id="41526-106">The service provider defines the meaning of these buffers.</span></span>

<span data-ttu-id="41526-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="41526-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="41526-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (Membros **dwDevSpecificSize** e **dwDevSpecificOffset** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="41526-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="41526-109">**TAPI 3. x:** Consulte [**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB \_ DEVSPECIFICBUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="41526-109">**TAPI 3.x:** See [**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB\_DEVSPECIFICBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
