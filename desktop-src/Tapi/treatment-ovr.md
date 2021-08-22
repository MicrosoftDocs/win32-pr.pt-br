---
description: O tratamento refere-se à manipulação de uma sessão de entrada que ainda não foi respondida ou foi colocada em espera, como música. Consulte as constantes do LINECALLTREATMENT \_ para obter uma lista de tratamentos definidos pela TAPI.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Tratamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f29f8848c76029daa7828f40061c828b625ec046dea7fac35159b390a4d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139739"
---
# <a name="treatment"></a>Tratamento

O tratamento refere-se à manipulação de uma sessão de entrada que ainda não foi respondida ou foi colocada em espera, como música. Consulte as [ \_ constantes do LINECALLTREATMENT](./linecalltreatment--constants.md) para obter uma lista de tratamentos definidos pela TAPI.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membro dwCallTreatment** de *lpCallInfo*)

**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** o membro cil \_ CALLTREATMENT** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
