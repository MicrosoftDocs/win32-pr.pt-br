---
description: O privilégio refere-se a se um aplicativo possui ou está monitorando a sessão.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4423b5eb1d50f5a7329726ab2e01040971daecca7e603247c49bcbc1d7c6d570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060574"
---
# <a name="privilege"></a>Privilege

O privilégio refere-se a se um aplicativo possui ou está monitorando a sessão. Se o aplicativo for proprietário da sessão, ele poderá executar uma variedade de operações de sessão. Se o aplicativo estiver apenas monitorando, ele receberá mensagens de estado e poderá acessar informações de sessão, mas qualquer tentativa de executar a maioria das operações resultará em um erro.

Durante a inicialização, um aplicativo informa à TAPI qual nível de privilégio ele requer em quais endereços. A TAPI oferece sessões de entrada somente para aplicativos que se registraram para privilégios de proprietário ou proprietário e monitor.

O privilégio de um aplicativo em uma sessão que ele cria é sempre proprietário.

**TAPI 2.x:** Consulte [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege membro** de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3.x:** Consulte [**ItCallInfo::get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o membro **CIL \_ NUMBEROFOWNERS** ou **CIL \_ NUMBEROFMONITORS** [**de CALLINFO \_ LONG.**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
