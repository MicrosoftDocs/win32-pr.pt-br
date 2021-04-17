---
description: A ID de chamada difere do identificador de sessão de duas maneiras primárias que o provedor de serviços a atribui, e é o mesmo para cada aplicativo que manipula a sessão.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: ID da chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784098"
---
# <a name="call-id"></a><span data-ttu-id="3b0de-103">ID da chamada</span><span class="sxs-lookup"><span data-stu-id="3b0de-103">Call ID</span></span>

<span data-ttu-id="3b0de-104">A ID de chamada difere do [identificador de sessão](session-identifier-ovr.md) de duas maneiras principais: o provedor de serviços a atribui e é o mesmo para cada aplicativo que manipula a sessão.</span><span class="sxs-lookup"><span data-stu-id="3b0de-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="3b0de-105">Ele não pode ser usado para comunicação comum com a TAPI em relação às operações de sessão porque não corresponde a um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="3b0de-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="3b0de-106">A ID de chamada é usada em operações, como determinar se um grupo de IDs de sessão realmente se refere a uma chamada, como é o caso de uma conferência ou para comunicações com outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b0de-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="3b0de-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="3b0de-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3b0de-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallID** da [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="3b0de-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="3b0de-109">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**membro \_ callid cil** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="3b0de-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
