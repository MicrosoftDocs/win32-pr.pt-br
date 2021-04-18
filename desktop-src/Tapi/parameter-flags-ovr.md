---
description: Os sinalizadores de parâmetro fornecem informações sobre uma variedade de sinalizadores de status em relação a uma sessão de comunicações, como se a identificação do chamador deve ser bloqueada. Consulte \_ constantes LINECALLPARAMFLAGS para obter uma lista de sinalizadores definidos pela TAPI.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Sinalizadores de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784086"
---
# <a name="parameter-flags"></a><span data-ttu-id="845d1-104">Sinalizadores de parâmetro</span><span class="sxs-lookup"><span data-stu-id="845d1-104">Parameter Flags</span></span>

<span data-ttu-id="845d1-105">Os sinalizadores de parâmetro fornecem informações sobre uma variedade de sinalizadores de status em relação a uma sessão de comunicações, como se a identificação do chamador deve ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="845d1-105">Parameter flags supply information on a variety of status flags concerning a communications session, such as whether caller identification should be blocked.</span></span> <span data-ttu-id="845d1-106">Consulte [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) para obter uma lista de sinalizadores definidos pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="845d1-106">See [LINECALLPARAMFLAGS\_ Constants](./linecallparamflags--constants.md) for a list of flags defined by TAPI.</span></span>

<span data-ttu-id="845d1-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="845d1-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="845d1-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallParamFlags** da *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="845d1-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallParamFlags** member of *lpCallInfo*).</span></span>

<span data-ttu-id="845d1-109">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLPARAMSFLAGS** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="845d1-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLPARAMSFLAGS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
