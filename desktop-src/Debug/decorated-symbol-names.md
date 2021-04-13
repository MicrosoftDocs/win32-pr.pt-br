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
# <a name="decorated-symbol-names"></a><span data-ttu-id="fa684-103">Nomes de símbolos decorados</span><span class="sxs-lookup"><span data-stu-id="fa684-103">Decorated Symbol Names</span></span>

<span data-ttu-id="fa684-104">Um nome de símbolo decorado inclui caracteres que distinguem como um símbolo público foi declarado.</span><span class="sxs-lookup"><span data-stu-id="fa684-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="fa684-105">Para \_ \_ funções stdcall, os nomes incluem o caractere "@" e um número decimal que especifica o número de bytes em seus parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="fa684-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="fa684-106">Por exemplo, o nome decorado da função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) é LoadLibrary@4 .</span><span class="sxs-lookup"><span data-stu-id="fa684-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="fa684-107">Para funções do C++, a decoração do nome é mais complexa e varia do compilador para o compilador.</span><span class="sxs-lookup"><span data-stu-id="fa684-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="fa684-108">Para recuperar o nome de símbolo não decorado, use a função [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .</span><span class="sxs-lookup"><span data-stu-id="fa684-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="fa684-109">Como alternativa, você pode chamar a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que o manipulador de símbolos sempre apresente símbolos com nomes não decorados.</span><span class="sxs-lookup"><span data-stu-id="fa684-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="fa684-110">Você deve definir essa opção antes de carregar os símbolos porque o manipulador de símbolos cria as tabelas de nome de símbolo em tempo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="fa684-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
