---
description: A Microsoft fornece separadores de palavras e lematizadores para vários idiomas. Este tópico descreve como implementar e usar separadores de palavras e lematizadores personalizados para idiomas e locais além daqueles fornecidos pela Microsoft.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implementando um separador de palavras e lematizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010386"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implementando um separador de palavras e lematizador

A Microsoft fornece separadores de palavras e lematizadores para vários idiomas. Este tópico descreve como implementar e usar separadores de palavras e lematizadores personalizados para idiomas e locais além daqueles fornecidos pela Microsoft.

> [!Note]
> A partir de julho de 2018, foi feita uma alteração de segurança no Windows Server 2019 que impede que DLLs sem uma assinatura da Microsoft sejam carregadas pelo SearchIndexer.exe. Como resultado, o Windows Server 2019 não oferece mais suporte a separadores de palavras personalizados assinados não Microsoft. 

Este tópico é organizado da seguinte maneira:

-   [Registrando uma DLL de recursos de idioma](#registering-a-language-resource-dll)
-   [Registrando um idioma](#registering-a-language-resource-dll)
-   [Implementando uma palavra Beaker](#implementing-a-word-beaker)
    -   [WordSink e PhraseSink](#wordsink-and-phrasesink)
    -   [Quebras](#breaks)
    -   [Escalabilidade, Performancy e segurança](#scalability-performancy-and-security)
-   [Implementando um lematizador](#implementing-a-stemmer)
    -   [Escalabilidade, Performancy e segurança](#scalability-performancy-and-security)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Registrando uma DLL de recursos de idioma

Cada DLL de recurso de idioma deve implementar e exportar os seguintes pontos de entrada. A DLL pode ser registrada para estar em qualquer pasta.

-   DllMain é o ponto de entrada padrão para DLL.
-   DllRegisterServer registra a DLL no registro, como `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   O DllCanUnloadNow permite que os clientes chamem esse ponto de entrada por meio de Component Object Model (COM) para determinar se é possível descarregar a DLL de recursos de idioma.
-   DllUnRegisterServer remove a DLL do registro.

## <a name="registering-a-language"></a>Registrando um idioma

O registro contém entradas específicas de idioma para o idioma que está sendo indexado e essas entradas controlam as partes dos processos de indexação e consulta específicos do idioma. Essas entradas de registro podem ser encontradas na seguinte chave do registro.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implementando uma palavra Beaker

Os separadores de palavras implementam [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker). O método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) executa todo o processamento e a análise de texto. Para implementar um componente de separador de palavras, você deve ter heurística de idioma para seu idioma. Isso inclui informações sobre sintaxe e morphology. Você também pode precisar de uma lista de palavras a serem excluídas ou incluídas. Você cria o arquivo de palavras de ruído para a localidade do idioma na lista de palavras excluídas. Para obter mais informações sobre considerações linguísticas e como essas considerações afetam as implementações de separador de palavras, consulte [considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md).

A principal finalidade do [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) é processar o texto continuamente da [**\_ fonte de texto**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) até que todo o texto seja processado ou até que o separador de palavras encontre um erro. No loop de processamento de dados, **IWordBreaker:: BreakText** chama a análise e os métodos de utilitário que executam tarefas específicas para esse processo. Por exemplo, o separador de palavras em alemão pode lidar com palavras compostas, enquanto o separador de palavras em francês pode processar [diacríticos](surface-form-normalization.md) ou [clitics](surface-form-normalization.md). As funções específicas que o separador de palavras executa e a estratégia que ele usa na execução dessas tarefas dependem totalmente dos requisitos para esse idioma.

Ao dividir o texto, os separadores de palavras identificam formulários "alternativos" para palavras que podem ter várias representações. Nenhuma relação semântica é implícita entre as palavras geradas. Na verdade, a palavra original pode não ser incluída entre a lista de alternativas. Os formulários alternativos são salvos na mesma posição no índice que a palavra original para indicar que eles são idênticos.

Quando um documento é incluído no índice, cada palavra recebe um valor inteiro que representa o deslocamento ou a distância da palavra do início de um documento. A distância relativa entre palavras em uma consulta é comparada com os deslocamentos armazenados no índice de texto completo. A consulta "onde está o documento do Kyle" corresponde a qualquer documento com "onde" no deslocamento n, "é" em n + 1, "Kyle" em n + 2 e "documento" em n + 3. "Onde está o documento do Kyle arquivado na base de dados?" é representado como:



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | Kyle Kyle<br/> | documento | arquiva | in  | o | banco de dados base<br/> |



 

Neste exemplo, o separador de palavras armazena formas alternativas para "Kyle" ("Kyle") e "Database" ("base de dados") no índice. O separador de palavras gera e armazena palavras alternativas durante o processo de criação de índice sob as seguintes condições:

-   Se for provável que uma palavra alternativa apareça como uma única palavra em uma consulta
-   Se não for provável que um lematizador derive a palavra original da alternativa

A geração de formulários alternativos do Word aumenta o número de formas pelas quais as consultas representam e correspondem a uma frase, conforme mostrado nas seguintes variações:

1.  Onde o documento Kyle é arquivado no banco de dados
2.  Onde está o documento do Kyle arquivado no banco de dados
3.  Onde o documento Kyle é arquivado no banco de dados
4.  Onde está o documento do Kyle arquivado no banco de dados

### <a name="wordsink-and-phrasesink"></a>WordSink e PhraseSink

Os separadores de palavras usam os objetos [**IWordSink**](iwordsink.md) e [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) para coletar e armazenar todas as palavras e frases que eles extraem do texto. Um separador de palavras armazena palavras em um formulário que é o mais próximo possível do formulário original do Word no documento. **IPhraseSink** armazena frases no momento da consulta. As frases melhoram a relevância dos resultados da consulta porque as seqüências de palavras mais longas são mais raras e fornecem maior distinção do que as frases menores. Quando o indexador coloca uma frase no **IPhraseSink** no momento da consulta, ele cria uma instância do separador de palavras para dividir a frase em palavras. Em seguida, o indexador avalia a frase verificando se as palavras na frase ocorrem adjacentes umas às outras no índice. Por exemplo, se "ABCD" ocorrer no índice nas posições *x*, *x*+ 1, *x*+ 2 e *x*+ 3, a correspondência de frase ocorrerá se qualquer subcadeia de caracteres adjacente "abcd" for enviada em uma consulta. Essa estratégia é eficaz para separadores de palavras com base em caracteres que dividem frases e palavras longas durante a criação do índice e que geram frases durante o tempo de consulta.

### <a name="breaks"></a>Quebras

As quebras são os espaços entre as palavras. Espaço em branco, pontuação, formatação ou apenas a natureza do próprio idioma pode causar interrupções. Há quatro tipos diferentes de quebras que o indexador usa: fim da palavra (EOW), fim da sentença (EOS), fim do parágrafo (EOP) e o fim do capítulo (EOC). A interrupção EOW é a interrupção padrão. Após cada token, cada quebra indica uma distância semântica diferente entre as palavras em cada lado. As palavras separadas por EOW têm o link semântico mais rígido, seguido por EOS, EOP e EOC. Várias chamadas para [**IWordSink::P utbreak**](iwordsink-putbreak.md) são cumulativas e são análogas à inserção de palavras ou frases nulas.

### <a name="scalability-performancy-and-security"></a>Escalabilidade, Performancy e segurança

A maneira como o separador de palavras responde a chamadas simultâneas é basicamente determinado pela sua escolha de modelo de Threading. O indexador é um aplicativo de thread único. Para que os separadores de palavras funcionem em um ambiente de thread único, os separadores de palavras devem ser escritos usando um modelo de Threading "gratuito" ou "ambos". Os separadores de palavras não devem se registrar com o COM usando o modelo de Threading "Apartment".

Recomendamos que os separadores de palavras evitem Estados globais e armazenem dados na instância para o separador de palavras. O único conteúdo que deve ser armazenado na implementação do separador de palavras é para os parâmetros *fQuery* e *ulMaxTokenSize*. Os separadores de palavras não devem ser mais do que duas vezes mais lentos do que o parâmetro de comparação estabelecido pelo separador de palavras em inglês. O desempenho do separador de palavras também deve melhorar com maior capacidade de hardware.

Os separadores de palavras para o indexador são executados no contexto de segurança do sistema local. Eles devem ser gravados para gerenciar buffers e para empilhar corretamente. Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteção contra estouros de buffer. Você sempre deve verificar o tamanho alocado do buffer e testar o tamanho dos dados em relação ao tamanho do buffer. Os separadores de palavras não podem pressupor que o texto passado para o método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) esteja bem formado. Para obter mais informações sobre como solucionar problemas de separadores de palavras, consulte [solução de problemas de recursos de idioma e práticas recomendadas](troubleshooting-language-resources.md).

## <a name="implementing-a-stemmer"></a>Implementando um lematizador

Os lematizadores implementam a interface [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) . O método [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) gera uma lista de formulários do formas flexionadas Word para uma determinada palavra de entrada. Para implementar um componente de lematizador, você deve ter heurística de idioma para seu idioma. Isso inclui informações sobre morphology. Você também pode precisar de uma lista de palavras a serem excluídas ou incluídas. Para obter mais informações sobre considerações linguísticas e como essas considerações afetam as implementações de lematizador, consulte [considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md).

Recomendamos que os lematizadores não devam gerar o caso de genitive, ou Possessive, para palavras. Por exemplo, "David" não é gerado como uma forma alternativa para "David ' s". O separador de palavras gera "David" e "David" quando analisa "David".

O lematizador usa o objeto [IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) para reunir a lista de palavras alternativas. [**IWordFormSink::P utword**](iwordformsink-putword.md) gera a palavra final do lematizador. Em todos os casos, essa palavra final é a mesma que a palavra de entrada de [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms). Por exemplo, considerando a palavra "nada", o lematizador gera as seguintes formas de palavra: "nadava", "Swimmer", "" nada "," "Swam" e "swum" por meio de chamadas para [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md). O lematizador gera "nada" por meio de **IWordFormSink::P utword**.

### <a name="scalability-performancy-and-security"></a>Escalabilidade, Performancy e segurança

Os lematizadores, como separadores de palavras, devem usar um modelo de Threading "gratuito" e registrar com com o modelo de Threading definido como "gratuito" ou "ambos". O Windows Search chama instâncias separadas do lematizador de threads diferentes ao mesmo tempo. Os lematizadores devem, portanto, ter dados mínimos de instância.

A precisão do lematizador tem um impacto significativo na relevância da consulta. Se o lematizador truncar o texto incorretamente, as consultas poderão retornar resultados imprevisíveis e imprecisos. Os lematizadores devem lidar com centenas de consultas por segundo sem afetar negativamente o desempenho da consulta. O desempenho do lematizador deve melhorar com o aumento do recurso de hardware. Para obter informações sobre como solucionar problemas de lematizadores, consulte [Solucionando problemas de recursos de linguagem e práticas recomendadas](troubleshooting-language-resources.md).

Os lematizadores da pesquisa do Windows são executados no contexto de segurança local. Eles devem ser gravados para gerenciar buffers e para empilhar corretamente. Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteção contra estouros de buffer. Você sempre deve verificar o tamanho alocado do buffer e testar o tamanho dos dados em relação ao tamanho do buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Noções básicas sobre componentes de recursos de idioma](understanding-language-resource-components.md)
</dt> <dt>

[Considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solucionando problemas de recursos de idioma e práticas recomendadas](troubleshooting-language-resources.md)
</dt> </dl>

 

 
