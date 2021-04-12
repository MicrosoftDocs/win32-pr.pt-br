---
description: O número do tronco no qual a chamada é roteada. Esse membro é usado para chamadas de entrada e saída.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Trunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170777"
---
# <a name="trunk"></a>Trunk

O número do tronco no qual a chamada é roteada. Esse membro é usado para chamadas de entrada e saída.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o membro de **\_ tronco cil** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
