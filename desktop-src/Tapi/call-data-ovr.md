---
description: Os dados de chamada são um buffer de tamanho de várias variantes que pode ser usado para acumular informações sobre uma sessão de comunicações. Essas informações ficam disponíveis para todos os aplicativos que possuem ou monitoram a sessão.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Dados de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296601"
---
# <a name="call-data"></a>Dados de chamada

Os dados de chamada são um buffer de tamanho de várias variantes que pode ser usado para acumular informações sobre uma sessão de comunicações. Essas informações ficam disponíveis para todos os aplicativos que possuem ou monitoram a sessão.

Por exemplo, o manipulador inicial de uma sessão de entrada pode solicitar e inserir informações de conta do cliente em um buffer de dados de chamada, e os manipuladores subsequentes não precisariam repetir a solicitação.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** e **DwCallDataOffset** Members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* set to LINECALLINFOSTATE \_ CALLDATA).

**TAPI 3. x:** Consulte [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** membro do [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent:: get \_ A causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) retorna o membro **\_ CALLDATA do CIC** da [**\_ causa CALLINFOCHANGE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
