---
description: Um nome de símbolo decorado inclui caracteres que distinguem como um símbolo público foi declarado.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nomes de símbolos decorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456877"
---
# <a name="decorated-symbol-names"></a>Nomes de símbolos decorados

Um nome de símbolo decorado inclui caracteres que distinguem como um símbolo público foi declarado. Para \_ \_ funções stdcall, os nomes incluem o caractere "@" e um número decimal que especifica o número de bytes em seus parâmetros de função. Por exemplo, o nome decorado da função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) é LoadLibrary@4 . Para funções do C++, a decoração do nome é mais complexa e varia do compilador para o compilador.

Para recuperar o nome de símbolo não decorado, use a função [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) . Como alternativa, você pode chamar a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que o manipulador de símbolos sempre apresente símbolos com nomes não decorados. Você deve definir essa opção antes de carregar os símbolos porque o manipulador de símbolos cria as tabelas de nome de símbolo em tempo de carregamento.

 

 
