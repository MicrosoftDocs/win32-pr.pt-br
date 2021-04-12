---
description: Quando necessário, a biblioteca DbgHelp foi ampliada para dar suporte às janelas de 32 e 64 bits.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Suporte atualizado à plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500954"
---
# <a name="updated-platform-support"></a>Suporte atualizado à plataforma

Quando necessário, a biblioteca DbgHelp foi ampliada para dar suporte às janelas de 32 e 64 bits. As definições de função e estrutura originais ainda estão em DbgHelp. h, mas também há versões atualizadas dessas definições que são compatíveis com o Windows de 64 bits. Se você usar as funções atualizadas em seu código, ele poderá ser compilado para o Windows de 32 e 64 bits. Seu código também será mais eficiente, pois as funções originais simplesmente chamam as funções atualizadas para executar o trabalho.

Por exemplo, DbgHelp. h contém definições para **SymUnloadModule** (função original) e **SymUnloadModule64** (função Updated). Essas definições são quase idênticas, mas usam tipos diferentes para o parâmetro *BaseOfDll* . (**SymUnloadModule** usa o tipo **DWORD** , enquanto **SymUnloadModule64** usa o tipo **DWORD64** .) Se você escrever seu código para usar o **SymUnloadModule64**, ele poderá ser compilado para o Windows de 32 e 64 bits. O código também é mais eficiente do que se fosse chamar **SymUnloadModule**.

Veja a seguir uma lista das funções atualizadas:

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

Veja a seguir uma lista das estruturas atualizadas:

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**\_Símbolo DEferido de imagehlp \_ \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**\_SYMBOL64 duplicado do imagehlp \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**LINE64 de IMAGEHLP \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**MODULE64 de IMAGEHLP \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**SYMBOL64 de IMAGEHLP \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



