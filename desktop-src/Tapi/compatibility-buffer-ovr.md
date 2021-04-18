---
description: O buffer de compatibilidade é específico para o padrão ISDN Q. 931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Buffer de compatibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756999"
---
# <a name="compatibility-buffer"></a><span data-ttu-id="fe7ff-104">Buffer de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="fe7ff-104">Compatibility Buffer</span></span>

<span data-ttu-id="fe7ff-105">O buffer de compatibilidade é específico para o padrão ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="fe7ff-105">The compatibility buffer is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="fe7ff-106">Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.</span><span class="sxs-lookup"><span data-stu-id="fe7ff-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="fe7ff-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="fe7ff-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="fe7ff-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** e **dwLowLevelCompOffset** membros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="fe7ff-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize**, and **dwLowLevelCompOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="fe7ff-109">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** e **CIB \_ LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="fe7ff-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_HIGHLEVELCOMPATIBILITYBUFFER** and **CIB\_LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
