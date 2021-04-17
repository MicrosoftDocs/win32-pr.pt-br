---
description: As informações específicas do aplicativo permitem que os aplicativos transmitam cada uma das outras informações relacionadas a uma sessão por meio da TAPI. Essas informações não são interpretadas pela TAPI e o uso é totalmente definido pelos aplicativos.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Informações específicas do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811938"
---
# <a name="application-specific-information"></a><span data-ttu-id="8ff5e-104">Informações específicas do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8ff5e-104">Application-specific Information</span></span>

<span data-ttu-id="8ff5e-105">As informações específicas do aplicativo permitem que os aplicativos transmitam cada uma das outras informações relacionadas a uma sessão por meio da TAPI.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="8ff5e-106">Essas informações não são interpretadas pela TAPI e o uso é totalmente definido pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="8ff5e-107">Quando as informações específicas do aplicativo são alteradas por um aplicativo, a TAPI envia todos os outros aplicativos com privilégios de monitor ou proprietário na sessão, um evento indicando que ocorreu uma alteração.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="8ff5e-108">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="8ff5e-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="8ff5e-109">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro *dwAppSpecific* de *lpCallInfo*), [**LineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**mensagem \_ CALLINFO de linha**](./line-callinfo.md) (*dwParam1* definido como LINECALLINFOSTATE \_ APPSPECIFIC).</span><span class="sxs-lookup"><span data-stu-id="8ff5e-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="8ff5e-110">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (o membro **cil \_ APPSPECIFIC** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="8ff5e-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
