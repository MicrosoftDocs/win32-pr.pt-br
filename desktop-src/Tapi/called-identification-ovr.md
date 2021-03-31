---
description: Chamada identificação identifica o endereço de destino original para uma sessão. Em situações em que uma sessão foi redirecionada, encaminhada ou transferida, isso será diferente da identificação conectada.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Chamada identificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829127"
---
# <a name="called-identification"></a>Chamada identificação

Chamada identificação identifica o endereço de destino original para uma sessão. Em situações em que uma sessão foi redirecionada, encaminhada ou transferida, isso será diferente da [identificação conectada](connected-identification-ovr.md).

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** e **dwCalledIDAddressType** membros de *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLEDIDADDRESSTYPE** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cis \_ CALLEDIDNAME** e **cis \_ CALLEDIDNAME** Members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
