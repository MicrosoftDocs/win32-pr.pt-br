---
description: Os recursos de manipulação de símbolos da API DbgHelp evoluíram ao longo dos anos.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Símbolos públicos, globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bf93ec8f11d1cec9c5fec64e2479dd91ee5cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010152"
---
# <a name="public-global-and-local-symbols"></a>Símbolos públicos, globais e locais

Os recursos de manipulação de símbolos da API DbgHelp evoluíram ao longo dos anos. Para garantir que seu código funcione em uma variedade de cenários e forneça detalhes completos sobre os símbolos, use as funções mais recentes sempre que possível. Por exemplo, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) substitui [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) substitui [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)e [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) substitui [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Símbolos públicos

Versões iniciais do DbgHelp.dll suportadas examinando apenas símbolos públicos. Esses símbolos são gerados para qualquer item no código que deve ser exposto entre diferentes arquivos de origem. Eles também incluem todos os itens que são exportados para fora do módulo.

Os símbolos são inseridos na imagem ou armazenados separadamente em um arquivo. dbg ou. pdb. As únicas informações armazenadas são o nome e o endereço do símbolo. Os nomes estão disponíveis como nomes decorados. Para exibir nomes não decorados, chame a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com SYMOPT \_ UNDNAME ou use a função [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .

Observe que a API DbgHelp não foi inicialmente projetada para dar suporte a várias instâncias do mesmo símbolo dentro de um módulo. Isso ocorre porque os símbolos públicos são restritos a nomes exclusivos dentro de um módulo. Portanto, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) retorna apenas o primeiro símbolo que corresponde. Para recuperar todos os símbolos que correspondem, chame [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Símbolos globais e locais

As versões mais recentes do DbgHelp.dll dão suporte a símbolos globais e locais ao usar arquivos. pdb. Essas novas versões incluem funções estáticas, funções com escopo dentro de um arquivo de origem, parâmetros de função e variáveis locais. Quando o DbgHelp pesquisa um símbolo, ele verifica as tabelas de símbolo globais e locais antes de verificar a tabela de símbolos públicos. Isso ocorre porque há mais informações disponíveis para esses tipos de símbolos do que está disponível para símbolos públicos.

Os símbolos globais e locais são armazenados com nomes não decorados. Portanto, o \_ sinalizador SYMOPT UNDNAME não tem nenhum efeito. Para obter nomes de símbolo decorados, você deve usar o \_ sinalizador somente públicos SYMOPTs \_ . Isso faz com que o DbgHelp pesquise apenas os símbolos públicos.

Para exibir os símbolos locais ou parâmetros de função, chame a função [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) com o membro **InstructionOffset** da estrutura de [**quadro de \_ pilha \_ do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) definida como o endereço de qualquer símbolo de função. As chamadas subsequentes para [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) e [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) podem operar dentro do contexto desse endereço. Para fazer isso, defina o parâmetro *BaseOfDll* como **NULL** e omita o especificador de módulo do parâmetro *Name* ou *Mask* . Isso força o DbgHelp a Pesquisar símbolos correspondentes no escopo indicado por **SymSetContext**.

Para determinar se um símbolo é um parâmetro, verifique o membro **flags** da estrutura [**de \_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Se o símbolo for um parâmetro, o membro conterá o \_ parâmetro SYMFLAG. Se for um símbolo local, o membro conterá SYMFLAG \_ local.

 

 



