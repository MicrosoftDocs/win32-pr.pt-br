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
# <a name="privilege"></a>Privilege

Privilégio se refere a se um aplicativo é proprietário ou está monitorando a sessão. Se o aplicativo for proprietário da sessão, ele poderá executar uma variedade de operações de sessão. Se o aplicativo só estiver monitorando, ele receberá mensagens de estado e poderá acessar as informações da sessão, mas qualquer tentativa de executar a maioria das operações resultará em um erro.

Durante a inicialização, um aplicativo informa à TAPI qual nível de privilégio é necessário em quais endereços. A TAPI oferece sessões de entrada somente para aplicativos que se registraram para o proprietário ou para o proprietário e o privilégio de monitor.

O privilégio de um aplicativo em uma sessão que ele cria é sempre proprietário.

**TAPI 2. x:** Consulte [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), membro **dwCallPrivilege** de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ privilégio**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o membro **cil \_ NUMBEROFOWNERS** ou **cil \_ NUMBEROFMONITORS** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
