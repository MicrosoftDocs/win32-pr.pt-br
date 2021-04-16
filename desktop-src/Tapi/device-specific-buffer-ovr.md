---
description: Os buffers específicos do dispositivo podem fazer parte de uma implementação de provedores de serviço de operações estendidas. O provedor de serviços define o significado desses buffers.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Buffer específico do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779470"
---
# <a name="device-specific-buffer"></a>Buffer específico do dispositivo

Os buffers específicos do dispositivo podem fazer parte da implementação de operações estendidas de um provedor de serviços. O provedor de serviços define o significado desses buffers.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (Membros **dwDevSpecificSize** e **dwDevSpecificOffset** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Consulte [**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB \_ DEVSPECIFICBUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
