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
# <a name="call-id"></a>ID da chamada

A ID de chamada difere do [identificador de sessão](session-identifier-ovr.md) de duas maneiras principais: o provedor de serviços a atribui e é o mesmo para cada aplicativo que manipula a sessão. Ele não pode ser usado para comunicação comum com a TAPI em relação às operações de sessão porque não corresponde a um aplicativo específico.

A ID de chamada é usada em operações, como determinar se um grupo de IDs de sessão realmente se refere a uma chamada, como é o caso de uma conferência ou para comunicações com outro aplicativo.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallID** da [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**membro \_ callid cil** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
