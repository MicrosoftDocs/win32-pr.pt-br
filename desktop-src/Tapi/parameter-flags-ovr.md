---
description: Os sinalizadores de parâmetro fornecem informações sobre uma variedade de sinalizadores de status em relação a uma sessão de comunicações, como se a identificação do chamador deve ser bloqueada. Consulte \_ constantes LINECALLPARAMFLAGS para obter uma lista de sinalizadores definidos pela TAPI.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Sinalizadores de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959856"
---
# <a name="parameter-flags"></a>Sinalizadores de parâmetro

Os sinalizadores de parâmetro fornecem informações sobre uma variedade de sinalizadores de status em relação a uma sessão de comunicações, como se a identificação do chamador deve ser bloqueada. Consulte [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) para obter uma lista de sinalizadores definidos pela TAPI.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallParamFlags** da *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLPARAMSFLAGS** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
