---
description: Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpeza do manipulador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826292"
---
# <a name="symbol-handler-cleanup"></a>Limpeza do manipulador de símbolos

Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Essa função enumera todos os módulos carregados, libera cada módulo e libera a memória alocada para a lista de módulos. Depois de chamar **SymCleanup**, você não poderá usar o identificador de processo nas funções de tratamento de símbolos até chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



