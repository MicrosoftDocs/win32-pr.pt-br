---
description: A identificação conectada identifica a parte que realmente estava conectada. Isso pode ser diferente da identificação chamada se a chamada tiver sido divertida.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identificação conectada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297762"
---
# <a name="connected-identification"></a>Identificação conectada

A identificação conectada identifica a parte que realmente estava conectada. Isso pode ser diferente da identificação chamada se a chamada tiver sido divertida.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Confira [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **DwConnectedIDOffset**, **dwConnectedIDNameSize** e **dwConnectedIDNameOffset** membros de *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cil \_ CONNECTEDIDNAME** membro da [**\_ cadeia de caracteres CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
