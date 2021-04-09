---
description: 'As seguintes informações de erro e estado do VSS são gravadas no log de eventos do aplicativo:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Log de erros do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090445"
---
# <a name="vss-error-logging"></a>Log de erros do VSS

As seguintes informações de erro e estado do VSS são gravadas no log de eventos do aplicativo:

-   Erros do solicitante produzidos usando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Erros de gravador produzidos no usando a classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , incluindo métodos de substituição
-   Erros gerados pelo provedor padrão
-   Erros de serviço VSS gerados no provedor de coordenação, no gravador e na atividade do solicitante (como a geração de eventos)

Esses erros podem ter várias causas, incluindo um erro de programação em código de terceiros ou erros de configuração relacionados ao VSS.

Os drivers VSS e a funcionalidade de implementação de nível inferior gravam erros no log do sistema. Software de terceiros (solicitante, provedor, gravador) pode escolher o log do aplicativo, o log do sistema ou ambos, para gravar entradas do log de erros.

É recomendável que aplicativos de alto nível (como código de modo de usuário) usem o log do aplicativo. Aplicativos de nível inferior, como interfaces de hardware e drivers, devem usar o log do sistema.

 

 



