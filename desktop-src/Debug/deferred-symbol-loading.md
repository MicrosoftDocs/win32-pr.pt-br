---
description: Para conservar o tempo e a memória ao trabalhar com muitos arquivos de símbolo, use a função SymSetOptions para definir a opção de carregamento de símbolo deferido ( \_ cargas DEferidas de SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Carregamento de símbolo adiado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957145"
---
# <a name="deferred-symbol-loading"></a>Carregamento de símbolo adiado

Para conservar o tempo e a memória ao trabalhar com muitos arquivos de símbolo, use a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para definir a opção de carregamento de símbolo deferido ( \_ cargas deferidas de SYMOPT \_ ) e, em seguida, use a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) ou [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) para carregar símbolos adiados para todos os módulos. O manipulador de símbolo listará os símbolos que estão disponíveis para os módulos, mas não mapeará as informações de depuração na memória até que ela seja solicitada. Esse é o método preferencial para usar com eficiência os símbolos de depuração. Todas as funções que usam símbolos são afetadas pelo carregamento de símbolo adiado.

 

 



