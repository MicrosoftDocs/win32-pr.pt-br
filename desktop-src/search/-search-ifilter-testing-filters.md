---
description: O conjunto de testes IFilter valida seus manipuladores de filtro.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Testando manipuladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b77fe098c2413e4f582ebfd98985dd09bf0ab9b5fc2def85fc7e954804dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463085"
---
# <a name="testing-filter-handlers"></a>Testando manipuladores de filtro

O [**conjunto de testes IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valida seus manipuladores de filtro. O conjunto de testes faz isso chamando métodos [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e verificando os valores retornados quanto à conformidade com a especificação da interface **IFilter;** e verificar se os identificadores de partes são exclusivos e crescentes, que a interface **IFilter** se comporta de forma consistente após a nova inicialização e se todas as chamadas de método **IFilter** com parâmetros inválidos retornam códigos de erro esperados. Os programas do conjunto de testes também despejam a saída de um arquivo filtrado por um manipulador de filtro e verificam as informações de registro **de IFilter** no Registro.

Este tópico é organizado da seguinte forma:

- [Invocação de linha de comando](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Procedimento de teste IFilter](#ifilter-test-procedure)
  - [Teste de validação](#validation-test)
  - [Teste de consistência](#consistency-test)
  - [Teste de entrada inválido](#invalid-input-test)
  - [Testando diferentes configurações de IFilter](#testing-different-ifilter-configurations)
- [Garantir que os itens registrados são indexados](#ensuring-registered-items-get-indexed)
  - [Arquivo de log de exemplo](#sample-log-file)
  - [Arquivo de despejo de exemplo](#sample-dump-file)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

> [!NOTE]  
> Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtros for desinstalado. Não há nenhum mecanismo para encadear filtros. Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.

## <a name="command-line-invocation"></a>invocação Command-Line dados

O conjunto de testes [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) consiste em três aplicativos de linha de comando [ –ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)e [filtreg.exe](#filtregexe) e um arquivo de inicialização, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> No Windows 7 e posteriores, os filtros gravados em código gerenciado são explicitamente bloqueados. Os filtros DEVEM ser escritos em código nativo devido a possíveis problemas de versão do CLR (Common Language Runtime) com o processo em que vários complementos são executados.

### <a name="ifilttstexe"></a>ifilttst.exe

O ifilttst.exe executa vários testes para validar um manipulador de filtro. O exemplo a seguir ilustra como invocar o programa ifilttst.exe da linha de comando:


```
ifilttst /i test.htm /l /d /v 1
```

O exemplo executa as seguintes tarefas:

- Direciona o programa para filtrar o arquivo test.htm
- Redireciona as mensagens de log para test.htm.log
- Redireciona as mensagens de despejo para test.htm.dmp
- Define o detalhes como 1

Para que o comando anterior funcione, três arquivos devem estar localizados no diretório de trabalho atual: `test.htm` , [ifilttst.exe](#ifilttstexe)e [ifilttst.ini](#ifilttstini). As opções de linha de comando são listadas na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternar e possíveis variáveis</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i nome do arquivo</strong></td>
<td>O arquivo de entrada ou diretório a ser filtrado. O nome do arquivo pode conter os caracteres curinga <code>*</code> e <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>As mensagens de log são direcionadas para um arquivo em vez da tela. As mensagens de log descrevem os testes individuais executados e os resultados de aprovação/falha dos testes. O nome do arquivo de log é o mesmo que o nome do arquivo de entrada, mas com uma extensão .log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>As mensagens de despejo são direcionadas para um arquivo em vez da tela. Mensagens de despejo descrevem o conteúdo das partes. A estrutura da parte é despejada quando o nível de detalhes é 3. O nome do arquivo de despejo é o mesmo que o nome do arquivo de entrada, mas com uma extensão .dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Desabilite o registro em log. Esse sinalizador substitui a <code>/l</code> opção .</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Desabilite o despejo. Esse sinalizador substitui a <code>/d</code> opção .</td>
</tr>
<tr class="even">
<td><strong>/v integer</strong></td>
<td>O nível de detalhes. O padrão é 3.
<ul>
<li>0 - O teste registra apenas mensagens referentes a falhas de interface <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> específicas. O teste despeja o conteúdo da parte.</li>
<li>1 - O teste registra mensagens de aviso, bem como aquelas do nível 0.</li>
<li>2 - O teste registra em logs mensagens referentes a testes que foram aprovados, bem como aquelas do nível 1.</li>
<li>3 - O teste registra mensagens informativas, bem como as do nível 2. Além disso, o teste despeja a estrutura da parte.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t integer</strong></td>
<td>O número de threads a iniciar. O padrão é 1.</td>
</tr>
<tr class="even">
<td><strong>/r integer</strong>]</td>
<td>Filtra recursivamente subdireários. O parâmetro inteiro opcional especifica a profundidade para a qual a recursão deve ser exercido. Se nenhum inteiro for especificado ou se o inteiro for 0, será assumida a recursão completa. Por padrão, a profundidade de recursão é 1.</td>
</tr>
<tr class="odd">
<td><strong>/c integer</strong></td>
<td>O número de vezes a ser loop. Se o inteiro for 0, o teste será loop infinito. Por padrão, o teste é loop somente uma vez.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Você deve incluir um espaço entre a opção de linha de comando e o valor .

### <a name="filtdumpexe"></a>filtdump.exe

O filtdump.exe carrega um manipulador de filtro para um documento especificado e imprime a saída produzida pela [**DLL de IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) O exemplo a seguir ilustra como invocar o filtdump.exe programa.

```
filtdump filename.ext
```
Filtdump.exe usa o [método ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) para carregar a DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) apropriada para a extensão de nome de arquivo especificada e imprime os resultados. Por exemplo, o comando a seguir instrui filtdump.exe carregar o manipulador de filtro smpfilt.dll para a extensão .smp, extrair todo o texto e propriedades do arquivo myfile.smp e imprimir os resultados.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

O filtreg.exe inspecione as informações de instalação do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no Registro. Invoque o filtreg.exe da linha de comando digitando seu nome, como no exemplo a seguir.

```
filtreg
```

Filtreg.exe enumera todas as extensões de nome de arquivo que têm manipuladores de filtro associados a elas imprimindo a extensão de nome de arquivo e o nome da [**DLL IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para a extensão. Essa é uma maneira simples de verificar a instalação correta de um **IFilter.**

### <a name="ifilttstini"></a>ifilttst.ini

Uma interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é inicializada chamando o [**método IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) O **método IFilter::Init** assume os quatro parâmetros a seguir:

1. *Grfflags*
2. *cAttributes*
3. *aAttributes*
4. *Pdwflags*

O usuário do programa ifilttst.exe do conjunto de testes [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pode especificar os valores para esses parâmetros em um arquivo chamado ifilttst.ini. A tabela a seguir descreve as entradas no arquivo ifilttst.ini que especificam os três primeiros parâmetros (os parâmetros de entrada). Para obter um arquivo de exemplo, consulte [arquivo de ifilttst.ini de exemplo](#sample-ifilttstini-file).

> [!NOTE]  
> Não há nenhuma entrada de tabela para o parâmetro *pdwFlags* porque ele é um parâmetro de saída; Ele não precisa ter nenhum valor especial antes da chamada para o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

 | Entrada         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | Os nomes dos sinalizadores [**de \_ inicialização do IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) que devem ser Unidos pelo operador OR para formar o parâmetro *grfFlags* do método [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Os nomes dos sinalizadores devem estar em letras maiúsculas e na mesma linha.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Um inteiro decimal que representa o valor do parâmetro *cAttributes* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Essa entrada deve começar com *aAttributes* e deve ser diferente das outras entradas de *aAttributes* na seção. Os nomes válidos para a entrada *aAttributes* são: *aAttributes*, *aAttributes1*, *aAttributes2* e assim por diante. O primeiro token deve ser um GUID. O GUID deve ser formatado exatamente conforme ilustrado na `[Test3]` seção do [arquivo de ifilttst.ini de exemplo](#sample-ifilttstini-file). O segundo token pode ser um identificador de propriedade (PID) que consiste em um número em notação hexadecimal ou um ponteiro para uma grande cadeia de caracteres (LPWSTR). Um LPWStr pode ser especificado ao colocar a cadeia de caracteres entre aspas duplas, conforme ilustrado na `[Test6]` seção do arquivo de ifilttst.ini de exemplo. |

Se as entradas flags e *cAttributes* não forem especificadas, elas serão padronizadas como 0. Se você definir *cAttributes* igual a 2, deverá especificar dois nomes de *aAttributes* . Na `[Test5]` seção do exemplo, *cAttributes* é 1, mas nenhum *aAttributes* foi especificado. Em seguida, o teste chama o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) com *cAttributes* igual a 1 e *aAttributes* igual a **NULL**. Esse é um caso de teste útil porque provavelmente causará uma violação de acesso no método **IFilter:: init** .

Se ifilttst.exe não conseguir encontrar um arquivo chamado ifilttst.ini no diretório de trabalho, uma configuração padrão será usada para inicializar o objeto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . O exemplo a seguir ilustra a configuração padrão.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Arquivo de ifilttst.ini de exemplo

O arquivo de ifilttst.ini é organizado em seções, com o nome da seção entre colchetes. No exemplo, as seções são nomeadas `[Test1]` , `[Test2]` e assim por diante. Todos os nomes de seção devem ser exclusivos. O teste lê os valores da primeira seção e inicializa o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com esses valores. Em seguida, todos os testes são executados usando essa configuração de **IFilter** . Em seguida, o **IFilter** é liberado e reinicializado, usando parâmetros listados acima. O processo é repetido até que todas as configurações sejam testadas.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>Procedimento de teste do IFilter

Depois que o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tiver sido inicializado, o programa de ifilttst.exe conduzirá uma série de testes no **IFilter**. Além de seguir os procedimentos de teste do **IFilter** , certifique-se de que sua implementação do **IFilter** empregue práticas de código seguras. consulte "práticas de código de segurança para Windows search" em [implementando manipuladores de filtro na pesquisa do Windows](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Teste de validação

O teste de validação percorre o objeto uma parte por vez, verificando cada parte individual e todos os códigos de retorno. O teste de validação salva todas as estruturas de [**\_ partes de estatística**](/windows/win32/api/filter/ns-filter-stat_chunk) retornadas em uma lista.

O teste de validação verifica as seguintes condições:

- A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** as IDs de partes do idChunk devem ser exclusivas e crescentes.
- A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** o parâmetro flags é um estado de parte reconhecido, como o [**bloco**](/windows/win32/api/filter/ne-filter-chunkstate)de partes, o texto da parte \_ ou as constantes de valor CenabledHUNK \_ .
- A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*o parâmetro breaktype* é um tipo de quebra reconhecido (0, 1, 2, 3, 4).
- Se os atributos de inicialização do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) especificarem que o **IFilter** deve retornar apenas partes que contêm propriedades de tipo de valor interno, *idChunkSource* deverá ser igual a 0.
- Se a parte não for derivada, isto é, se não for uma propriedade de tipo de valor interno, então a [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* deve ser igual à **\_ parte de stat**.*idChunk*.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna S \_ OK ou outro valor de retorno aceitável, como filtrar \_ e \_ terminar \_ de \_ partes, filtrar \_ e \_ vincular \_ não disponível e assim por diante.
- Se a parte contiver texto, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornará s \_ OK, filtre o \_ \_ último \_ texto ou filtre \_ E \_ não \_ mais \_ texto.
- Se [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornar o filtro \_ S \_ Last Text \_ , a próxima chamada para **IFILTER:: gettext** retornará Filter \_ E \_ não \_ mais \_ texto.
- Se a parte contiver um valor, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornará S \_ OK ou filtrar \_ E \_ não \_ mais \_ valores.

### <a name="consistency-test"></a>Teste de consistência

O programa ifilttxt.exe reinicializa a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com os mesmos parâmetros do teste de validação e executa um teste de consistência. Se a implementação do **IFilter** tiver sido inicializada com o sinalizador [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ somente a indexação \_ , o teste liberará a interface **IFilter** e a associará novamente antes de fazer outra chamada para o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

O teste de consistência verifica as seguintes condições:

- Cada estrutura de [**\_ parte de estatística**](/windows/win32/api/filter/ns-filter-stat_chunk) retornada pelo método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) é idêntica à **\_ parte de stat** correspondente retornada no teste de validação.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna S \_ OK ou outro valor de retorno aceitável, como filtrar \_ e \_ terminar \_ de \_ partes, filtrar \_ e \_ vincular \_ não disponível e assim por diante.

### <a name="invalid-input-test"></a>Teste de entrada inválido

O programa ifilttst.exe reinicializa a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com os mesmos parâmetros e executa um teste de entrada inválido. Este teste percorre o documento uma parte de cada vez fazendo chamadas de função incorretamente, como chamar o método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) quando o Chuck atual contiver texto. O teste verifica todos os códigos de retorno quanto à conformidade com a especificação do **IFilter** .

O teste de entrada inválido verifica as seguintes condições:

- Se a parte atual contiver texto, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornará \_ um filtro e \_ nenhum valor \_ , e uma chamada para [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) terá sucesso.
- Se a parte atual contiver um valor, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornará Filter \_ E \_ nenhum \_ texto e uma chamada para [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) terá sucesso.
- Se a chamada anterior para [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornou \_ um filtro e \_ não \_ mais \_ texto, chamadas sucessivas para **IFilter:: gettext** retornarão o filtro \_ e \_ não \_ mais \_ texto.
- Se a chamada anterior para [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornou \_ um filtro e \_ não \_ mais \_ valores, as chamadas sucessivas para **IFilter:: GetValue** retornarão o filtro \_ e \_ não \_ mais \_ valores.
- Se a chamada anterior para [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retornou o filtro \_ e o \_ final \_ de \_ partes, chamadas sucessivas para **IFilter:: GetChunk** filtro \_ de retorno e \_ final \_ das \_ partes.

> [!NOTE]  
> O teste de entrada inválido compara as estruturas de partes atuais com as retornadas no teste de validação para garantir que elas sejam idênticas.

### <a name="testing-different-ifilter-configurations"></a>Testando diferentes configurações de IFilter

O programa ifilttst.exe libera a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e religa, desta vez inicializando-a com o próximo conjunto de parâmetros. O teste repete o ciclo: teste de validação, teste de consistência e teste de entrada inválido, até que todas as configurações de **IFilter** desejadas especificadas no arquivo de [ifilttst.ini](#ifilttstini) tenham sido testadas.

## <a name="ensuring-registered-items-get-indexed"></a>Garantindo que os itens registrados sejam indexados

O teste final de seu [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garante que o **IFilter** seja registrado corretamente e que seja invocado para indexar os itens que você registrou para usá-lo. Você pode usar o Gerenciador de catálogo para iniciar a reindexação ou usar o Gerenciador de escopo de rastreamento (CSM) para configurar as regras padrão que indicam as URLs que você deseja que o indexador rastreie. após a conclusão da indexação, use a interface do usuário do Windows search para procurar uma cadeia de caracteres no conteúdo ou nas propriedades de itens. Se os itens foram indexados, eles serão exibidos nos resultados da pesquisa.

Para obter mais informações sobre a reindexação, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md). O exemplo de código ReindexMatchingUrls demonstra maneiras de especificar quais arquivos reindexar e como. O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação do Gerenciador de escopo de rastreamento (CSM). Ambos os exemplos de código estão disponíveis em [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>Arquivo de log de exemplo

Mediante solicitação, o programa de Ifilttst.exe pode produzir um log contendo uma descrição das etapas que ele executa durante a execução. Os exemplos a seguir são trechos de um arquivo de log, com o detalhamento definido para o valor 3 mais alto possível.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

A primeira linha é uma mensagem informativa, indicando que uma nova configuração foi carregada a partir do arquivo de ifilttst.ini. Linha (3) indica o nome da seção no arquivo de ifilttst.ini do qual a configuração atual foi lida. Linhas (4) a (7) liste os parâmetros para [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init). As linhas que começam com `INFO` são mensagens informativas sobre a associação do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e o início do teste de validação. As linhas que começam com `PASS` são mensagens relacionadas a testes específicos que passaram.

A linha no exemplo de log a seguir é um aviso. Os avisos chamam a atenção para o comportamento do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que é problemático, embora seja legal. Esse aviso indica que o método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retornou uma parte de texto que não contém texto.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

O exemplo de mensagem de erro a seguir indica que o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitiu uma parte que não foi solicitada.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

No caso desse exemplo de mensagem de erro, o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitiu uma parte com um PID de `0x5` . A inspeção da seção `[Test1]` no ifilttst.ini mostraria que o **IFilter** foi configurado para não emitir partes com esse PID. Por exemplo, se nenhum IFILTER \_ init \_ aplicar \_ \_ atributos de índice nem o IFilter \_ init \_ aplicar \_ outros \_ atributos foram especificados na entrada flags e, se *cAttributes* fosse 0, o **IFILTER** emitiria apenas partes com um PID `0x13` e correspondente ao \_ conteúdo PID STG \_ .

### <a name="sample-dump-file"></a>Exemplo de arquivo de despejo

Mediante solicitação, o programa de Ifilttst.exe pode produzir um despejo contendo as partes encontradas e seu conteúdo. O exemplo a seguir é um trecho desse arquivo de despejo.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

As nove primeiras linhas descrevem a estrutura da parte atual. O GUID e o PID correspondem ao \_ conteúdo do armazenamento PSGUID/PID \_ STG \_ . Esta é uma parte que contém texto sem formatação. O texto está na seguinte estrutura de partes:

```
10. This is an HTML IFilter test page
```

A próxima parte, começando na linha 11, tem um GUID diferente, correspondente ao `HTML IFilter` e um PID diferente, correspondente a um href HTML. Essa é uma propriedade de tipo de valor interno, exportada pelo `HTML IFilter` .

A próxima parte, começando na linha 21, tem o mesmo GUID e PID, mas seu estado de parte é `VALUE` em vez de `TEXT` . Observe que o texto nessas duas últimas partes é igual ao da primeira parte. Mas como o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) foi projetado para três atributos (texto sem-formato, HTML HREF como texto e HTML HREF como um valor) a serem aplicados a essa frase, os resultados são emitidos em três partes separadas.

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample,](-search-sample-ifiltersample.md) disponível [no GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md).
- Para uma visão geral dos tipos de arquivo, consulte [Tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e Registro de Aplicativo.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Sobre manipuladores de filtro na Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para criar manipuladores de filtro na Windows Search](-search-3x-wds-extidx-filters.md)

[Retornando propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[Manipuladores de filtros que são Windows](-search-ifilter-implementations.md)

[Implementando manipuladores de filtro na Windows Search](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
