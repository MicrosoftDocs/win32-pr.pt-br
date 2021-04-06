---
description: O código de país ou região é relevante somente quando o tipo de endereço é LINEADDRESSTYPE \_ PHONENUMBER. Ele identifica uma área do mundo.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Código de país ou região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827381"
---
# <a name="country-or-region-code"></a>Código de país ou região

O código de país ou região é relevante somente quando o tipo de endereço é LINEADDRESSTYPE \_ PHONENUMBER. Ele identifica uma área do mundo.

Todos os provedores de serviço que dão suporte ao uso de números de telefone devem dar suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCountryCode** da *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ COUNTRYCODE** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
