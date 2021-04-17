---
description: As informações de cobrança são específicas para o padrão ISDN Q. 931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: Informações de cobrança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766237"
---
# <a name="charging-information"></a><span data-ttu-id="417ec-104">Informações de cobrança</span><span class="sxs-lookup"><span data-stu-id="417ec-104">Charging Information</span></span>

<span data-ttu-id="417ec-105">As informações de cobrança são específicas para o padrão ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="417ec-105">Charging information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="417ec-106">Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.</span><span class="sxs-lookup"><span data-stu-id="417ec-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="417ec-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="417ec-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="417ec-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (Membros **dwChargingInfoSize** e **dwChargingInfoOffset** de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="417ec-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** and **dwChargingInfoOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="417ec-109">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ CHARGINGINFOBUFFER** membro of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="417ec-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_CHARGINGINFOBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
