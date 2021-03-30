---
title: Manipulando erros de RAS
description: Quando ocorre um erro, o Gerenciador de conexões de acesso remoto invoca o manipulador de notificação do cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS do serviço de acesso remoto, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636691"
---
# <a name="handling-ras-errors"></a>Manipulando erros de RAS

Quando ocorre um erro, o Gerenciador de conexões de acesso remoto invoca o manipulador de notificação do cliente. A notificação indica o estado da conexão quando o erro ocorreu e um código que identifica o erro. Nesses casos, o manipulador de notificação deve chamar [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para encerrar a conexão RAS.

Os códigos de erro que identificam erros de RAS são definidos no arquivo Raserror. h. O cliente RAS pode usar a função [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obter uma cadeia de caracteres de exibição que descreve o erro. Consulte [códigos de erro de roteamento e acesso remoto](routing-and-remote-access-error-codes.md) para obter uma descrição desses erros.

 

 




