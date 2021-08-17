---
description: Os recursos de manipulação de símbolos da API DbgHelp evoluiram ao longo dos anos.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Símbolos públicos, globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406096"
---
# <a name="public-global-and-local-symbols"></a>Símbolos públicos, globais e locais

Os recursos de manipulação de símbolos da API DbgHelp evoluiram ao longo dos anos. Para garantir que seu código funcione em uma variedade de cenários e fornece detalhes completos sobre os símbolos, use as funções mais novas sempre que possível. Por exemplo, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) substitui [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) substitui [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)e [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) substitui [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Símbolos públicos

As versões iniciais DbgHelp.dll com suporte ao exame apenas de símbolos públicos. Esses símbolos são gerados para qualquer item no código que deve ser exposto entre arquivos de origem diferentes. Eles também incluem todos os itens exportados para fora do módulo.

Os símbolos são inseridos na imagem ou armazenados separadamente em um arquivo .dbg ou .pdb. As únicas informações armazenadas são o nome e o endereço do símbolo. Os nomes estão disponíveis como nomes decorados. Para exibir nomes não rateados, chame a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com SYMOPT UNDNAME ou use a \_ [**função UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)

Observe que a API DbgHelp não foi inicialmente projetada para dar suporte a várias instâncias do mesmo símbolo em um módulo. Isso porque os símbolos públicos são restritos a nomes exclusivos em um módulo. Portanto, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) retorna apenas o primeiro símbolo que corresponde. Para recuperar todos os símbolos que corresponderem, [**chame SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Símbolos globais e locais

As versões mais recentes DbgHelp.dll suporte a símbolos globais e locais ao usar arquivos .pdb. Essas novas versões incluem funções estáticas, funções com escopo dentro de um arquivo de origem, parâmetros de função e variáveis locais. Quando DbgHelp pesquisa um símbolo, ele verifica as tabelas de símbolos globais e locais antes de verificar a tabela de símbolos pública. Isso porque há mais informações disponíveis para esses tipos de símbolos do que para símbolos públicos.

Símbolos globais e locais são armazenados com nomes não rateados. Portanto, o sinalizador SYMOPT \_ UNDNAME não tem nenhum efeito. Para obter nomes de símbolo decorados, você deve usar o sinalizador SYMOPT \_ PUBLICS \_ ONLY. Isso faz com que DbgHelp pesquise apenas os símbolos públicos.

Para exibir símbolos locais ou parâmetros de função, chame a função [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) com o membro **InstructionOffset** da estrutura [**IMAGEHLP \_ STACK \_ FRAME**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) definida como o endereço de qualquer símbolo de função. Chamadas subsequentes [**para SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) e [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) podem operar dentro do contexto desse endereço. Para fazer isso, de definir o *parâmetro BaseOfDll* como **NULL** e omitir o especificador de módulo do *parâmetro Name* *ou Mask.* Isso força DbgHelp a procurar símbolos correspondentes dentro do escopo indicado por **SymSetContext.**

Para determinar se um símbolo é um parâmetro, verifique o **membro Flags** da estrutura [**SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Se o símbolo for um parâmetro, o membro conterá SYMFLAG \_ PARAMETER. Se for um símbolo local, o membro conterá SYMFLAG \_ LOCAL.

 

 



