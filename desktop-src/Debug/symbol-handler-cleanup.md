---
description: Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpeza do manipulador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956955"
---
# <a name="symbol-handler-cleanup"></a>Limpeza do manipulador de símbolos

Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Essa função enumera todos os módulos carregados, libera cada módulo e libera a memória alocada para a lista de módulos. Depois de chamar **SymCleanup**, você não poderá usar o identificador de processo nas funções de tratamento de símbolos até chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



