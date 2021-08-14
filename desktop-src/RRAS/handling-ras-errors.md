---
title: Tratando erros de RAS
description: Quando ocorre um erro, o Gerenciador de Conexões remoto invoca o manipulador de notificação do cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS do Serviço de Acesso Remoto, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b870678eb2dbe95c190bc67415b9abb5481c33918429194404893349c0d7f7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791274"
---
# <a name="handling-ras-errors"></a>Tratando erros de RAS

Quando ocorre um erro, o Gerenciador de Conexões remoto invoca o manipulador de notificação do cliente. A notificação indica o estado da conexão quando ocorreu o erro e um código que identifica o erro. Nesses casos, o manipulador de notificação deve chamar [**RasUp para**](/windows/desktop/api/Ras/nf-ras-rashangupa) encerrar a conexão RAS.

Os códigos de erro que identificam erros ras são definidos no arquivo raserror.h. O cliente RAS pode usar a [**função RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obter uma cadeia de caracteres de exibição que descreve o erro. Consulte [Códigos de erro de roteamento e acesso](routing-and-remote-access-error-codes.md) remoto para ver uma descrição desses erros.

 

 




