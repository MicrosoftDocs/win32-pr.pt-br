---
description: As informações de cobrança são específicas para o padrão ISDN Q. 931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: Informações de cobrança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766237"
---
# <a name="charging-information"></a>Informações de cobrança

As informações de cobrança são específicas para o padrão ISDN Q. 931. Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (Membros **dwChargingInfoSize** e **dwChargingInfoOffset** de *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ CHARGINGINFOBUFFER** membro of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
