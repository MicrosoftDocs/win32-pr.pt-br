---
description: As seções a seguir contêm uma lista alfabética de funções agrupadas por área. As informações de cada função incluem uma lista dos Estados de chamada válidos na entrada da função e transições de estado de chamada típicas quando a solicitação é concluída.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funções TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505914"
---
# <a name="tapi-functions"></a>Funções TAPI

As seções a seguir contêm uma lista alfabética de funções agrupadas por área. As informações de cada função incluem uma lista dos Estados de chamada válidos na entrada da função e transições de estado de chamada típicas quando a solicitação é concluída.

-   [Funções de telefonia assistidas](assisted-telephony-functions.md)
-   [Funções do Call Center](call-center-functions.md)
-   [Funções de dispositivo de linha](line-device-functions.md)
-   [Funções de dispositivo de telefone](phone-device-functions.md)

Para funções TAPI categorizadas por nível de serviço e tarefa, consulte [referência de função rápida TAPI](tapi-quick-function-reference.md).

Observe que as limitações do provedor de serviços podem existir em relação aos Estados reais em que uma função pode ser executada. Os aplicativos devem verificar o membro **dwCallFeatures** na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , o membro **dwAddressFeatures** na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) e o membro **dwLineFeatures** na estrutura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para determinar se uma função é permitida ou não no estado de chamada atual.

 

 



