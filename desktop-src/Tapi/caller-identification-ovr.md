---
description: A identificação do chamador fornece informações sobre a entidade de chamada ao receber uma sessão de entrada. Um aplicativo geralmente usa esses dados como parte de uma mensagem de status para um usuário.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificação do chamador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829126"
---
# <a name="caller-identification"></a>Identificação do chamador

A identificação do chamador fornece informações sobre a entidade de chamada ao receber uma sessão de entrada. Um aplicativo geralmente usa esses dados como parte de uma mensagem de status para um usuário.

Essas informações nem sempre estão disponíveis imediatamente. Um aplicativo que deseja usar essas informações e verificou que o provedor de serviços dá suporte a ela deve verificar várias vezes antes de presumir que as informações não estão disponíveis.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** e **dwCallerIDAddressType** membros de *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLERIDADDRESSTYPE** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cis \_ CALLERIDNAME** e **cis \_ CALLERIDNAME** Members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
