---
description: Um nome de símbolo decorado inclui caracteres que distinguem como um símbolo público foi declarado.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nomes de símbolo decorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60432788b69f0c8779030f32a190ccfb55859434f714a13f769b328ee246a309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076410"
---
# <a name="decorated-symbol-names"></a>Nomes de símbolo decorados

Um nome de símbolo decorado inclui caracteres que distinguem como um símbolo público foi declarado. Para funções stdcall, os nomes incluem o caractere "@" e um número decimal que especifica o número de \_ \_ bytes em seus parâmetros de função. Por exemplo, o nome decorado da [**função LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) é LoadLibrary@4 . Para funções C++, a decoração de nome é mais complexa e varia de compilador para compilador.

Para recuperar o nome do símbolo indecoerdo, use a [**função UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) Como alternativa, você pode chamar a [**função SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que o manipulador de símbolos sempre apresente símbolos com nomes não rateados. Você deve definir essa opção antes de carregar os símbolos porque o manipulador de símbolos cria as tabelas de nomes de símbolo no tempo de carregamento.

 

 
