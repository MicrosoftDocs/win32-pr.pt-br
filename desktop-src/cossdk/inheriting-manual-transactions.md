---
description: Herdando transações manuais
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Herdando transações manuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0042b7bb1e1545c44c44149c4605c9aabcbcc12fecebb974eb97f95da087b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896006"
---
# <a name="inheriting-manual-transactions"></a>Herdando transações manuais

Se um objeto com uma transação de BYOT em seu contexto criar um segundo objeto, o objeto downstream poderá herdar a transação de BYOT (se configurada para herdar transações). O primeiro objeto criado usando o gateway BYOT precisa ser configurado para transações "exigir" ou "suporte". Os objetos subsequentes na atividade podem ser configurados com base nos requisitos do aplicativo.

Para transações automáticas, o tempo de execução do COM+ não tenta confirmar a transação até que o objeto raiz indique que ele está pronto (chamando [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) antes de retornar de uma chamada). Os usuários devem estar cientes de que uma transação de BYOT pode ser confirmada prematuramente (pois o trabalho de objetos filho não foi concluído), porque a "raiz" não está sendo executada no ambiente de tempo de execução do COM+ e a semântica de confirmação não está vinculada ao tempo de vida do objeto. Em geral, o usuário deve tomar cuidado para não violar o limite de sincronização da transação.

Caso contrário, a semântica de confirmação COM+ se aplicará. O COM+ não tentará confirmar uma transação enquanto um objeto dentro de um limite de sincronização estiver em chamada. Além disso, os objetos podem indicar sua consistência usando [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit). Se for feita uma tentativa de confirmar uma transação que inclui o trabalho de um objeto chamado **DisableCommit**, a transação será anulada.

 

 



