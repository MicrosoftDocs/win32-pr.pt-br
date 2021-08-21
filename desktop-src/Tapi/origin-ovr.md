---
description: Origin é uma descrição geral de onde a sessão foi iniciada, como se ela é externa ou interna a uma rede corporativa. Consulte LineCALLORIGIN Constants (Constantes LINECALLORIGIN) \_ para ver uma lista de origens compatíveis com a TAPI.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a1f4dafd2b4a3ee85b3a05b3c8ab8f95656237b0ad5bf292c53a5bbb2d3bed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002824"
---
# <a name="origin"></a>Origem

Origin é uma descrição geral de onde a sessão foi iniciada, como se ela é externa ou interna a uma rede corporativa. Consulte [LineCALLORIGIN \_ Constants (Constantes LINECALLORIGIN)](./linecallorigin--constants.md) para ver uma lista de origens compatíveis com a TAPI.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwOrigin** membro de *lpCallInfo*).

**TAPI 3.x:** Consulte [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**membro CIL \_ ORIGIN** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
