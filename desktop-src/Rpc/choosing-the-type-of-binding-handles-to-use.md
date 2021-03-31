---
title: Escolhendo o tipo de identificadores de associação a ser usado
description: Escolhendo o tipo de identificadores de associação a ser usado
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005232"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Escolhendo o tipo de identificadores de associação a ser usado

**Prática recomendada:** Se você souber qual servidor será usado pelo aplicativo, use identificadores explícitos. Se você não fizer isso, use identificadores explícitos constructos todas as vezes ou use identificadores genéricos com rotinas de **\_ associar** e **\_ desassociar** .

Não use identificadores implícitos ou identificadores automáticos. Os identificadores implícitos não são thread-safe e, embora a segurança de thread possa parecer desnecessária, ela pode ser necessária mais tarde. Os identificadores automáticos têm grande sobrecarga e exigem muita configuração para funcionar corretamente. Seus recursos de pesquisa foram substituídos por serviços Active Directorys.

Os identificadores explícitos são altamente eficientes e muitos recursos atraentes estão disponíveis apenas para identificadores explícitos. Por exemplo, se várias chamadas RPC forem para o mesmo servidor, você poderá construir o identificador de associação uma vez e fazer todas as chamadas com ele. Essa abordagem é muito mais eficiente do que qualquer outro método. Se o servidor ao qual a chamada será desconhecido, construa um identificador de ligação explícito para cada chamada ou use identificadores de associação genéricos.

No Microsoft™ Windows XP, o tempo de execução de RPC é bastante eficiente na reutilização e no cache de chamadas, portanto, se a chamada *n*+ 1º terminar no mesmo servidor que a chamada *n* th, o RPC reutilizará os recursos alocados para a chamada *n*, burlando a necessidade de armazenar em cache identificadores de associação para melhorar o desempenho.

 

 




