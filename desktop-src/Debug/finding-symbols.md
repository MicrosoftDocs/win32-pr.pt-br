---
description: Depois que um arquivo de símbolo é carregado no manipulador de símbolo, um aplicativo pode usar as funções de localizador de símbolos para retornar informações de símbolo para um endereço especificado.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Localizando símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90aae9d2894ca8abc7470b2068b508655a50bcb76e1a122f2307f81273abec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912689"
---
# <a name="finding-symbols"></a>Localizando símbolos

Depois que um arquivo de símbolo é carregado no manipulador de símbolo, um aplicativo pode usar as funções de localizador de símbolos para retornar informações de símbolo para um endereço especificado. Essas funções também podem encontrar um nome de arquivo de código-fonte e um local de número de linha para um endereço.

## <a name="enumerating-symbol-files"></a>Enumerando arquivos de símbolo

Para recuperar uma lista de todos os arquivos de símbolo carregados pelo nome do módulo, chame a função [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) . Para obter um exemplo, consulte [enumerando módulos de símbolo](enumerating-symbol-modules.md). Para recuperar uma lista de símbolos para um determinado módulo, chame a função [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) . Para obter um exemplo, consulte [enumerando símbolos](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Recuperando símbolos por endereço

Para recuperar informações simbólicas para um endereço específico, use a função [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Essa função recupera informações e as armazena em uma estrutura de [**\_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Como os nomes de símbolo são variáveis de comprimento, você deve fornecer espaço de buffer adicional após a declaração de estrutura de **\_ informações de símbolo** . Para obter um exemplo, consulte [recuperando informações de símbolo por endereço](retrieving-symbol-information-by-address.md).

Observe que o endereço não precisa estar em um limite de símbolo. Se o endereço vier após o início de um símbolo, mas antes do final do símbolo (o início do símbolo mais o tamanho do símbolo), a função localizará o símbolo.

## <a name="retrieving-symbols-by-symbol-name"></a>Recuperando símbolos por nome de símbolo

Para recuperar informações simbólicas em uma estrutura de [**\_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) para um nome de módulo e símbolo específico, use a função [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Se o carregamento de símbolos deferido for definido, o **SymFromName** tentará carregar o arquivo de símbolo para um módulo se ele ainda não tiver sido carregado. Para especificar um nome de módulo junto com um nome de símbolo, use o *módulo* sintaxe! *SymName*. O caractere "!" delimita o nome do módulo do nome do símbolo. Para obter um exemplo, consulte [recuperando informações de símbolo por nome](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Recuperando números de linha por endereço

Para recuperar o local do código-fonte de um endereço específico, use a função [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) . Essa função preenche uma [**estrutura \_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) que inclui o nome do arquivo de origem e o local do número de linha referenciado pelo endereço especificado. Para obter um exemplo, consulte [recuperando informações de símbolo por endereço](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Recuperando números de linha por nome de símbolo

Para recuperar o local do código-fonte de um nome de símbolo específico, use a função [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) . Essa função é semelhante a [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), mas recupera uma estrutura de [**\_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) . Para usar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) ou **SymGetLineFromName64**, você deve definir a opção carregar linhas (SYMOPT \_ carregar \_ linhas) usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Para obter um exemplo, consulte [recuperando informações de símbolo por nome](retrieving-symbol-information-by-name.md).

 

 



