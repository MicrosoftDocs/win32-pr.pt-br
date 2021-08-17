---
description: Para remover os contadores de desempenho dos aplicativos do sistema, execute as etapas a seguir.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Excluindo contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144009"
---
# <a name="deleting-performance-counters"></a>Excluindo contadores de desempenho

Para remover os contadores de desempenho do aplicativo do sistema, execute as etapas a seguir.

1.  Use a **ferramenta unlodctr** incluída no computador para remover os dados relacionados ao contador do Registro. Observe que a chave de desempenho **do** aplicativo deve existir para que a **ferramenta unlodctr** seja bem-sucedida. Para obter detalhes, [consulte Removendo nomes de contadores e descrições do Registro](removing-counter-names-and-descriptions-from-the-registry.md).
2.  **Exclua as** **chaves desempenho e** vinculação na chave serviços **do** aplicativo. Para excluir essas chaves, use o utilitário Regedt32.exe ou chame [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
