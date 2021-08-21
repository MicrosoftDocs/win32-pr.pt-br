---
description: A identificação do chamador fornece informações sobre a parte de chamada ao receber uma sessão de entrada. Um aplicativo normalmente usa esses dados como parte de uma mensagem de status para um usuário.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificação do chamador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3e4e412af29664d5a3585ad783545c13991250db8c449901db07868ea8feb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870000"
---
# <a name="caller-identification"></a>Identificação do chamador

A identificação do chamador fornece informações sobre a parte de chamada ao receber uma sessão de entrada. Um aplicativo normalmente usa esses dados como parte de uma mensagem de status para um usuário.

Essas informações nem sempre estão disponíveis imediatamente. Um aplicativo que deseja usar essas informações e verificou que o provedor de serviços dá suporte a ela deve verificar várias vezes antes de assumir que as informações não estão disponíveis.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** e **dwCallerIDAddressType membros** *de lpCallInfo*).

**TAPI 3.x:** Consulte [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**membro CIL \_ CALLERIDADDRESSTYPE** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**membros DE CIS \_ CALLERIDNAME** e **CIS \_ CALLERIDNAME** de [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
