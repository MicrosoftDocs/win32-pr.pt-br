---
description: Quando um aplicativo redireciona uma sessão, a TAPI retém informações de identificação sobre o local que redirecionou a sessão e o local para o qual ela foi redirecionada.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Redirecionar identificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060444"
---
# <a name="redirect-identification"></a>Redirecionar identificação

Quando um aplicativo [redireciona](redirect-ovr.md) uma sessão, a TAPI retém informações de identificação sobre o local que redirecionou a sessão e o local para o qual ela foi redirecionada.

"Redirecionando" refere-se ao local que invocou a operação de redirecionamento. "Redirecionamento" identifica o novo destino para a sessão.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** e **dwRedirectingIDNameOffset** membros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)chamado com o **cis \_ REDIRECTIONIDNAME**, **cis \_ REDIRECTIONIDNUMBER**, **cis \_ REDIRECTINGIDNAME** ou o **membro \_ REDIRECTINGIDNUMBER do CIS** da [**cadeia de \_ caracteres CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
