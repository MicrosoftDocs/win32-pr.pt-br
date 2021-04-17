---
description: Privilégio se refere a se um aplicativo é proprietário ou está monitorando a sessão.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782900"
---
# <a name="privilege"></a><span data-ttu-id="23232-103">Privilege</span><span class="sxs-lookup"><span data-stu-id="23232-103">Privilege</span></span>

<span data-ttu-id="23232-104">Privilégio se refere a se um aplicativo é proprietário ou está monitorando a sessão.</span><span class="sxs-lookup"><span data-stu-id="23232-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="23232-105">Se o aplicativo for proprietário da sessão, ele poderá executar uma variedade de operações de sessão.</span><span class="sxs-lookup"><span data-stu-id="23232-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="23232-106">Se o aplicativo só estiver monitorando, ele receberá mensagens de estado e poderá acessar as informações da sessão, mas qualquer tentativa de executar a maioria das operações resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="23232-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="23232-107">Durante a inicialização, um aplicativo informa à TAPI qual nível de privilégio é necessário em quais endereços.</span><span class="sxs-lookup"><span data-stu-id="23232-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="23232-108">A TAPI oferece sessões de entrada somente para aplicativos que se registraram para o proprietário ou para o proprietário e o privilégio de monitor.</span><span class="sxs-lookup"><span data-stu-id="23232-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="23232-109">O privilégio de um aplicativo em uma sessão que ele cria é sempre proprietário.</span><span class="sxs-lookup"><span data-stu-id="23232-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="23232-110">**TAPI 2. x:** Consulte [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), membro **dwCallPrivilege** de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="23232-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="23232-111">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ privilégio**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o membro **cil \_ NUMBEROFOWNERS** ou **cil \_ NUMBEROFMONITORS** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="23232-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
