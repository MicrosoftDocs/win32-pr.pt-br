---
description: Origin é uma descrição geral de onde a sessão foi iniciada, como se ela é externa ou interna a uma rede corporativa. Consulte \_ constantes LINECALLORIGIN para obter uma lista de origens às quais a TAPI dá suporte.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71105caff17850c76c1e2c388911086a4cf9ea8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091617"
---
# <a name="origin"></a>Origem

Origin é uma descrição geral de onde a sessão foi iniciada, como se ela é externa ou interna a uma rede corporativa. Consulte [ \_ constantes LINECALLORIGIN](./linecallorigin--constants.md) para obter uma lista de origens às quais a TAPI dá suporte.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwOrigin** da *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (membro da **\_ origem da cil** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
