---
title: Lidando com as definições em arquivos IDL
description: Esta página descreve por que os símbolos definidos com um \ define desaparecem dos arquivos H gerados pelo compilador de MIDL e o que pode ser feito sobre ele. Esta explicação se aplica a todos os arquivos processados pelo MIDL, como \. idl, \. ACF, arquivos \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL do compilador MIDL, lidando com as definições
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005474"
---
# <a name="dealing-with-defines-in-idl-files"></a>Lidando com as \# definições em arquivos IDL

Esta página descreve por que os símbolos definidos com uma **\# definição** desaparecem dos arquivos H gerados pelo compilador de MIDL e o que pode ser feito sobre ele. Essa explicação se aplica a todos os arquivos processados pelo MIDL, como \* . idl, \* . ACF, \* arquivos. h.

O desaparecimento de **\# definir** símbolos é resultado de MIDL delegando o pré-processamento de arquivos de entrada para um pré-processador. Por padrão, o pré-processador é um pré-processador de C/C++ do ambiente de compilação. Após o pré-processamento, o MIDL do fluxo de entrada recebe apenas as \# diretivas de pré-processador de linha. Em particular, o pré-processador desverte todas as definições de macro em arquivos de entrada e, portanto, o MIDL não pode detectar sua presença. Consequentemente, quando MIDL Replica definições de tipo de um arquivo de entrada para o arquivo H gerado, as \# Defines não são replicadas. Portanto, não use \# define diretamente em arquivos IDL se eles forem usados posteriormente a partir do arquivo H gerado.

As quatro soluções alternativas a seguir são recomendadas:

-   Use a especificação de Declaração [**const**](const.md) .
-   Use arquivos de cabeçalho separados que são importados ou incluídos no arquivo IDL, e posteriormente incluídos no código-fonte C.
-   Use constantes de enumeração no arquivo IDL.
-   Use [**a \_ cotação de CPP**](cpp-quote.md) para reproduzir **\# definir** no arquivo de cabeçalho gerado.

Você pode reproduzir constantes de manifesto usando a **sintaxe de declaração constante de IDL**. Observe que [**const**](const.md) na declaração de constante de IDL é diferente da semântica **const** C/C++ e simplesmente introduz uma constante nomeada para uma compilação de IDL. Por exemplo:

``` syntax
const short ARRSIZE = 10
```

Este exemplo especifica que **ARRSIZE** é uma constante com um valor de 10. As constantes nomeadas podem ser usadas em declaradores de matriz de IDL e em outros locais onde um programador de C usaria um manifesto definido. Além disso, essa sintaxe resulta na geração da seguinte linha no arquivo de cabeçalho:

``` syntax
#define ARRSIZE 10
```

Outra maneira de lidar com **\#** instruções de definição é empacotá-las em um arquivo de cabeçalho separado, em um arquivo dedicado para **\#** definir instruções ou em um arquivo que contenha apenas definições de tipo. Um arquivo que contém apenas diretivas de pré-processador pode ser incluído com segurança pelo arquivo IDL e pelos arquivos de origem C. Embora as diretivas não estejam disponíveis no arquivo de cabeçalho gerado pelo compilador MIDL, o programa de origem C pode incluir o arquivo de cabeçalho separado. De maneira semelhante, um arquivo de cabeçalho com **\#** instruções de definição e de tipo regular pode ser importado de seu arquivo IDL. Essa abordagem encapsula as **\#** instruções define e typedef usando-as em um arquivo H, de modo que os **\#** símbolos de definição não sejam usados diretamente no arquivo de importação de IDL. Importar um cabeçalho ou arquivo IDL para outro arquivo IDL impede que as instruções typedef sejam replicadas para o arquivo H gerado pelo MIDL (que está em contraste com as **\#** instruções include). Essa abordagem permite que o arquivo de cabeçalho original seja referenciado com segurança do código C ao longo do arquivo H gerado sem ter um problema com definições duplicadas.

O uso de constantes de enumeração no arquivo IDL também é eficaz. Essas constantes podem ser usadas em expressões constantes em IDL, por exemplo, em declaradores de matriz. As constantes de enumeração não são removidas durante as primeiras fases da compilação MIDL pelo pré-processador do compilador C, portanto, as constantes de enumeração estão disponíveis no arquivo de cabeçalho gerado pelo compilador MIDL. Considere o seguinte instrução:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Essa instrução não será removida durante a compilação MIDL pelo pré-processador C e o typedef será replicado para o arquivo H gerado. A constante MAXSTRINGCOUNT está disponível para programas de origem C que incluem o arquivo de cabeçalho gerado pelo compilador MIDL.

Por fim, a diretiva de [**\_ citação de CPP**](cpp-quote.md) do MIDL pode ser usada para gravar uma cadeia de caracteres arbitrária diretamente no arquivo H gerado. Por exemplo, para obter a constante de manifesto usada anteriormente nesta página com **\_ aspas de CPP**, a instrução a seguir pode ser usada:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Essa instrução resulta na geração da seguinte linha no arquivo de cabeçalho:

``` syntax
#define ARRSIZE 10
```

 

 




