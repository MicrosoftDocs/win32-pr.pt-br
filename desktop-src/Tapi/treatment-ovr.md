---
description: O tratamento refere-se à manipulação de uma sessão de entrada que ainda não foi respondida ou foi colocada em espera, como música. Consulte as constantes do LINECALLTREATMENT \_ para obter uma lista de tratamentos definidos pela TAPI.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Tratamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbde0e602836b543e849afb3d56c33fd6df0a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461275"
---
# <a name="treatment"></a><span data-ttu-id="dbd6e-104">Tratamento</span><span class="sxs-lookup"><span data-stu-id="dbd6e-104">Treatment</span></span>

<span data-ttu-id="dbd6e-105">O tratamento refere-se à manipulação de uma sessão de entrada que ainda não foi respondida ou foi colocada em espera, como música.</span><span class="sxs-lookup"><span data-stu-id="dbd6e-105">Treatment refers to the handling of an incoming session that has not yet been answered or has been put on hold, such as music.</span></span> <span data-ttu-id="dbd6e-106">Consulte as [ \_ constantes do LINECALLTREATMENT](./linecalltreatment--constants.md) para obter uma lista de tratamentos definidos pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="dbd6e-106">Please see [LINECALLTREATMENT\_ Constants](./linecalltreatment--constants.md) for a list of treatments defined by TAPI.</span></span>

<span data-ttu-id="dbd6e-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="dbd6e-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="dbd6e-108">**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membro dwCallTreatment** de *lpCallInfo*)</span><span class="sxs-lookup"><span data-stu-id="dbd6e-108">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** member of *lpCallInfo*)</span></span>

<span data-ttu-id="dbd6e-109">**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** o membro cil \_ CALLTREATMENT** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="dbd6e-109">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_CALLTREATMENT** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
