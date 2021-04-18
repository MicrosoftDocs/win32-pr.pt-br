---
description: A sintaxe de consulta avançada (AQS) é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Usando a sintaxe de consulta avançada programaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802124"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Usando a sintaxe de consulta avançada programaticamente

A sintaxe de consulta avançada (AQS) é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa. O AQS é empregado por desenvolvedores para criar consultas programaticamente (e por usuários para restringir seus parâmetros de pesquisa). O AQS canônico foi introduzido no Windows 7 e deve ser usado no Windows 7 e posterior para gerar programaticamente consultas AQS.

Este tópico é organizado da seguinte maneira:

-   [Sobre a sintaxe de consulta avançada](#about-advanced-query-syntax)
    -   [Exemplos](#examples)
    -   [Propriedades](#properties)
-   [Uso de palavra-chave em idiomas locais](#keyword-use-in-local-languages)
-   [Sintaxe de consulta avançada canônica no Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [Exemplos](#examples)
    -   [Operadores de consulta](#query-operators)
    -   [Valores de consulta](#query-values)
-   [Restrições de escopo](#scope-restrictions)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-advanced-query-syntax"></a>Sobre a sintaxe de consulta avançada

Uma consulta consiste em consultas básicas conectadas com AND, OR e NOT, conforme mostrado na seguinte sintaxe de exemplo:

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> AQS não diferencia maiúsculas de minúsculas, com exceção de AND, OR e NOT, que deve estar em letras maiúsculas.

 

Se uma consulta tiver dois ou mais usos de e ou ou, elas serão vinculadas da esquerda para a direita, independentemente de ser e ou ou. Ou seja, a consulta, "Apple e pêra ou Black", será interpretada como se fosse escrita como "(Apple e pêra) ou Black", e a consulta, "Apple ou pêra e Black", será interpretada como se fosse escrita como "(Apple ou pêra) e Black". Portanto, se um documento contiver a palavra Black, mas nem a Apple, nem a pera, a primeira consulta a retornará, mas a segunda consulta não será. Portanto, recomendamos que você use parênteses explícitos para qualquer consulta que combine e e ou para evitar erros ou interpretações indesejadas.

Uma consulta básica procura itens que atendam a uma restrição sobre uma propriedade. A única parte necessária de uma consulta básica é a restrição ou o valor de pesquisa. Se você não especificar uma propriedade, o Windows Search pesquisará todas as propriedades. <restr> representa a restrição de pesquisa.

Os seguintes formulários para uma consulta básica são válidos:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Uma propriedade é designada por uma palavra-chave como autor ou tamanho, ou por um nome de propriedade canônica, como [System. DateModified](../properties/props-system-datemodified.md). Os formulários válidos para uma propriedade são os seguintes:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Um operador indica uma operação como < ou =. Para obter uma lista de operadores válidos, consulte a seção operadores de consulta mais adiante neste tópico.

Uma restrição básica é uma restrição simples em uma propriedade que pode ser gravada sem parênteses:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Uma restrição é um valor de pesquisa, como um valor numérico ou um valor de cadeia de caracteres, opcionalmente com um operador. Os formulários válidos para uma restrição são os seguintes:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Se você não especificar um operador, o Windows Search escolherá o operador mais apropriado para sua consulta:

-   Para uma propriedade de cadeia de caracteres, o operador de COP \_ Word \_ STARTSWITH $< é assumido.
-   Para todas as outras propriedades, o \_ operador COP equal = é assumido.

Para o uso programático de AQS, é recomendável que você sempre tenha um operador explícito. A forma válida para pesquisar um valor ou intervalo de valores simples é a seguinte:

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

Um valor simples pode consistir em qualquer um dos seguintes tipos:

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>Exemplos

Uma consulta que pesquisa um documento que contém a fase "último trimestre", criada por Theresa ou Lee, e que foi salva na pasta mydocs, combina três consultas básicas da seguinte maneira:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

As três consultas básicas são:

-   "último trimestre"
-   Autor: (Theresa ou Lee)
-   pasta: mydocs

Uma consulta básica que usa sintaxe canônica é:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Propriedades

As propriedades são referenciadas por uma palavra-chave, que pode ser um nome de propriedade canônica no Windows 7 e posterior. AQS na interface do usuário do Windows pode usar o rótulo em vez do nome da propriedade canônica, como autor, em vez de [System. Author](../properties/props-system-author.md). No Windows Vista e versões anteriores, era possível usar os rótulos em inglês, independentemente do idioma da interface do usuário. No Windows 7 e posterior, o Windows Search reconhece palavras-chave somente no idioma da interface do usuário padrão atual.

### <a name="support-for-custom-properties"></a>Suporte para propriedades personalizadas

No Windows Vista e versões anteriores, as propriedades personalizadas não estavam disponíveis em AQS. No Windows 7 e posterior, o AQS funciona com propriedades personalizadas registradas com o sistema de propriedades. Para obter mais informações sobre como criar propriedades personalizadas, consulte [sistema de propriedades](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Propriedades de DateTime no Windows 8

A partir do Windows 8, as propriedades de DateTime (como [System. DateModified](../properties/props-system-datemodified.md)) dão suporte ao formato canônico de data e hora especificado por [ISO-8601](https://www.w3.org/TR/NOTE-datetime), incluindo, opcionalmente, o fuso horário UTC.

-   **Windows 8 e anterior, data e hora sem fuso horário UTC:** *aaaa* - *mm* - *ddThh*:*mm*:*SS*

    Esse formato especifica uma hora local, independentemente da localidade do usuário ou do sistema.

-   **Windows 8, data e hora com fuso horário UTC:** *yyyy* - *mm* - *ddThh*:*mm*:*ssTZD*

    Este formato especifica uma hora no fuso horário UTC especificado.

## <a name="keyword-use-in-local-languages"></a>Uso de palavra-chave em idiomas locais

No Windows 7 e versões posteriores, as palavras-chave mnemônicos funcionam apenas no idioma do sistema, como palavras-chave do alemão somente em um sistema operacional alemão e palavras-chave em inglês apenas em um sistema operacional em inglês. [System. Author](../properties/props-system-author.md) é uma palavra-chave canônica, e o valor mnemônico para a propriedade System. Author é autor, por exemplo. A introdução de palavras-chave canônicas compensa o fato de que as palavras-chave mnemônicos inglesas não são mais reconhecidas universalmente em todos os sistemas operacionais, independentemente da linguagem, como era o caso no Windows Vista e versões anteriores.

> [!Note]  
> No Windows 7 e posterior, o Windows Search reconhece palavras-chave somente no idioma padrão atual e não em inglês, a menos que o inglês seja o padrão atual. Recomendamos que os desenvolvedores sempre usem a sintaxe canônica para que seu aplicativo não tenha problemas de idioma com palavras-chave.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Sintaxe de consulta avançada canônica no Windows 7

A sintaxe canônica foi introduzida para palavras-chave no Windows 7. Um exemplo de uma consulta com uma propriedade canônica é `System.Message.FromAddress:=me@microsoft.com` . Ao codificar consultas em aplicativos em execução no Windows 7 e posterior, você deve usar a sintaxe canônica para gerar consultas AQS programaticamente. Se você não usar a sintaxe canônica e seu aplicativo for implantado em uma localidade ou idioma da interface do usuário diferente do idioma no código do aplicativo, suas consultas não serão interpretadas corretamente.

As convenções para a sintaxe de palavra-chave canônica são as seguintes:

-   A sintaxe canônica de uma propriedade é seu nome canônico, como `System.Photo.LightSource` . Os nomes canônicos não diferenciam maiúsculas de minúsculas.
-   A sintaxe canônica para os operadores boolianos consiste nas palavras-chave AND, OR e NOT, em letras maiúsculas.
-   Os operadores <, >, = e assim por diante, não são localizados e, portanto, também fazem parte da sintaxe canônica.
-   Se uma propriedade `P` tiver valores enumerados ou intervalos chamados N ₁ por meio de NK, a sintaxe canônica para o valor ou o intervalo será o nome canônico de P, seguido pelo caractere \# , seguido de N<sub>I</sub>, conforme ilustrado no exemplo a seguir:
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` e assim por diante.
-   Para um tipo de semântica definido T com valores ou intervalos denominados N ₁ por meio de NK, a sintaxe canônica para o valor ou intervalo *é o nome* canônico para T, seguido pelo caractere \# , seguido de N <sub>I</sub>, conforme ilustrado no exemplo a seguir:
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Para valores literais como palavras ou frases, a sintaxe canônica é a mesma que a sintaxe regular. Exemplos de consultas com valores literais em sintaxe canônica:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> Não há sintaxe canônica para números no Windows 7 e posterior. Como os formatos de ponto flutuante variam entre as localidades, o uso de uma consulta canônica que envolve uma constante de ponto flutuante não é suportado. As constantes de inteiro, por outro lado, podem ser escritas usando apenas dígitos (sem separadores para milhares) e podem ser usadas com segurança em consultas canônicas no Windows 7 e versões posteriores.

 

### <a name="examples"></a>Exemplos

A tabela a seguir mostra alguns exemplos de propriedades canônicas e a sintaxe para usá-las.



| Tipo de propriedade canônica | Exemplo                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor da cadeia de caracteres               | [System.Author](../properties/props-system-author.md)<br/>    | O valor da cadeia de caracteres é procurado na propriedade autor: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Intervalo de enumeração          | [System. Priority](../properties/props-system-priority.md)             | A propriedade Priority pode ter um intervalo de valores numéricos:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System. IsDeleted](../properties/props-system-isdeleted.md)<br/> | Valores Boolianos podem ser usados com qualquer propriedade booleana:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True` e `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numérico                  | [Sistema. tamanho](../properties/props-system-size.md)<br/>      | Não é possível gravar com segurança uma consulta canônica que envolve uma constante de ponto flutuante, pois os formatos de ponto flutuante variam entre as localidades. Os inteiros devem ser escritos sem separadores para milhares. Por exemplo:<br/>`System.Size:<12345` |



 

Para obter mais informações sobre propriedades canônicas e o sistema de propriedades em geral, consulte [Propriedades do sistema](../properties/props.md). Como alternativa, consulte os arquivos de cabeçalho públicos.

### <a name="query-operators"></a>Operadores de Consulta

Se uma propriedade, p, tiver vários valores para algum item, uma consulta AQS para p: <restr> retornará o item se <restr> for **verdadeira** para pelo menos um dos valores. ( <restr> representa uma restrição.)

A sintaxe listada na tabela a seguir consiste em um operador, símbolo de operador, exemplo e descrição de exemplo. O operador e o símbolo podem ser usados em qualquer idioma e incluídos em qualquer consulta. Não use os operadores de COP \_ \_ \_ . Alguns dos operadores têm símbolos intercambiáveis.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operador</th>
<th>Símbolo</th>
<th>Exemplo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System. FileExtension: = &quot; . txt&quot;<br/></td>
<td>O valor é String &quot; <em>. txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System. Kind: imagem ≠<br/> System. Photo. DateTaken:-[] ¹<br/> Sistema. Kind: &lt; &gt; imagem<br/> Sistema. tipo: não Picture<br/> Sistema. Kind:--imagem<br/></td>
<td>A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem.<br/> A propriedade <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> tem um valor.<br/> A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem. <br/> A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem. <br/> Os operadores duplos não aplicados à mesma propriedade não são cancelados. Portanto, System. Kind:--Picture é equivalente a System. Kind:-Picture e System. Kind: não Picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. Size: &lt; 1 KB<br/></td>
<td>Esse valor é menor que <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System. Data: &gt; System. StructuredQueryType. DateTime # hoje<br/></td>
<td>Este valor é maior que <em>hoje</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. Size: &lt; = 1 KB<br/></td>
<td>Esse valor é menor ou igual a <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. Size: &gt; = 1 KB<br/></td>
<td>Esse valor é igual a ou maior que <em>1 KB</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System. FileName: ~ &lt; &quot; instruções C++&quot;<br/></td>
<td>Localiza os itens em que o nome do arquivo começa com os caracteres de &quot; <em>introdução do C++</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System. Photo. CameraModel: ~ &gt; não<br/></td>
<td>Localiza itens em que o valor da propriedade termina com os caracteres <em>não</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System. Subject. ~ = round <br/> System. Search. autosummary: ~ ~ redondo<br/></td>
<td>Localiza uma mensagem que tem essa cadeia de caracteres no assunto e que corresponderá a &quot; g regras de<em>ida</em> e volta, &quot; por exemplo.<br/> Localiza todos os itens com um resumo resumido que contém os caracteres <em>arredondados</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author: ~! &quot; Sanjay&quot;<br/></td>
<td>Localiza os autores que não têm a sequência de caracteres &quot; <em>Sanjay</em> &quot; neles.<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System. FileName: ~ &quot; MIC? osoft W * d&quot;<br/></td>
<td>Localiza os arquivos em que o nome do arquivo começa com o <em>MIC</em>, seguido por algum caractere, seguido por <em>osoft w</em>, seguido de todos os caracteres que terminam com <em>d</em>. <br/> O ? e * os caracteres não são interpretados literalmente e funcionam como caracteres curinga de estilo DOS:<br/>
<ul>
<li>? corresponde a um caractere arbitrário.</li>
<li>* corresponde a zero ou mais caracteres arbitrários.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System. StructuredQuery. virtual. from: $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>Para o Windows 7 e posterior. Localiza a frase &quot; <em>Sanjay Jacobs</em> &quot; em todas as propriedades. A palavra <em>Sanjay</em> deve ser seguida da palavra <em>Jacobs</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author: $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Para o Windows 7 e posterior. Localiza qualquer item em que o autor contém uma palavra que começa com os caracteres &quot; <em>San</em> &quot; .<br/> Localiza qualquer arquivo no qual o nome do arquivo contenha uma palavra começando com <em>micro</em>, seguido por uma palavra que começa com <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

¹ colchetes vazios ( \[ \] ) denotam "sem valor".

Para propriedades de cadeia de caracteres, a operação padrão é COP \_ Word \_ começa \_ com ou COP \_ Word \_ Equals.

### <a name="query-values"></a>Valores de consulta

Exemplos úteis de como os valores de consulta podem ser restritos estão listados na tabela a seguir.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor/símbolo</th>
<th>Exemplos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>auto<br/></td>
<td>Qualquer sequência de caracteres que possa ser pesquisada. A cadeia de caracteres não deve conter combinações de espaço em branco ou caracteres que fazem parte da sintaxe. Este exemplo pesquisa uma palavra que começa com <em>auto</em>.<br/></td>
</tr>
<tr class="even">
<td>Cadeia de caracteres entre aspas &quot;&quot;</td>
<td>&quot;Conclusões: válidas para &quot; &quot; a &quot; &quot; &quot; &quot; equipe azul&quot;<br/></td>
<td>Qualquer sequência de caracteres. A cadeia de caracteres não é interpretada como parte da sintaxe.<br/> As aspas podem ser incluídas em uma consulta se forem duplicadas. Este exemplo pesquisa <em>a &quot; &quot; equipe azul</em>.<br/></td>
</tr>
<tr class="odd">
<td>Integer</td>
<td>5678<br/></td>
<td>Use apenas dígitos para inteiros. Não use separadores para milhares.<br/></td>
</tr>
<tr class="even">
<td>Número de ponto flutuante</td>
<td>5678,1234<br/></td>
<td>Como os formatos de ponto flutuante variam entre as localidades, uma consulta canônica não pode usar uma constante de ponto flutuante. O uso de sintaxe canônica com números de ponto flutuante não é seguro para localização. <br/></td>
</tr>
<tr class="odd">
<td>Booliano <strong>verdadeiro</strong> / <strong>falso</strong></td>
<td>System. IsRead: = System. StructuredQueryType. Boolean # true<br/> System. IsEncrypted:-System. StructuredQueryType. Boolean # false<br/></td>
<td>O valor booliano <strong>verdadeiro</strong> .<br/> O valor booliano <strong>false</strong> .<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System. Keywords: = []<br/></td>
<td>Colchetes vazios denotam que não há nenhum valor. Este exemplo localiza todos os itens que não foram marcados. <br/></td>
</tr>
<tr class="odd">
<td>Datas absolutas</td>
<td>System. @ Date: 1/26/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>Localiza itens com uma data de 26 de janeiro de 2010.<br/> Localiza itens que foram modificados em 15 de outubro de 2002 entre as horas 19:00:00 e 19:00:59. <br/>
<blockquote>
[!Note]<br />
Como os formatos de data (como formatos de ponto flutuante) variam entre as localidades, o uso da sintaxe canônica com datas absolutas não é suportado e não é seguro para localização.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Datas relativas</td>
<td>System. Data: System. StructuredQueryType. DateTime # hoje<br/> System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth<br/> System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear<br/></td>
<td>Localiza itens com a data de hoje.<br/> Localiza itens com uma data no próximo mês.<br/> Localiza itens com uma data no último ano.<br/>
<blockquote>
[!Note]<br />
Além de Pesquisar datas específicas e intervalos de datas, o AQS reconhece valores de datas relativas (como <em>hoje</em>, <em>amanhã</em>, <em>nextweek</em>, <em>nextmonth</em>) e dia (como <em>terça-feira</em> ou segunda-feira). <em> Quarta-feira</em>) e mês (<em>fevereiro</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System. @ Date: 11/05/04.. 11/10/04 sistema. Size: 5 KB.. 10 KB<br/></td>
<td>Pontos duplos indicam um intervalo de valores. Localiza itens com uma data entre 11/05/04 e 11/10/04, inclusive.<br/> Localiza itens entre 5 e 10 KB de tamanho.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Restrições de escopo

Os usuários podem limitar o escopo de suas pesquisas a locais de pasta ou armazenamentos de dados específicos. Por exemplo, se você usar várias contas de email e quiser limitar uma consulta ao Microsoft Outlook ou ao Microsoft Outlook Express, poderá usar `System.Search.Store:mapi` ou `System.Search.Store:oe` respectivamente. A tabela a seguir mostra alguns exemplos de como restringir uma pesquisa por armazenamento de dados.



| Restringir pesquisa por repositório de dados  | Palavra-chave | Exemplo                                     |
|--------------------------------|---------|---------------------------------------------|
| Arquivos                          | arquivo    | System. Search. Store: arquivo                    |
| Outlook                        | MAPI    | System. Search. Store: MAPI                    |
| Outlook Express                | OE      | System. Search. Store: OE                      |
| Arquivos Offline                  | CSC     | System. Search. Store: CSC                     |
| Pasta específica na unidade local | folder  | System. ItemFolderNameDisplay: C: " \\ MyFolder" |



 

## <a name="additional-resources"></a>Recursos adicionais

-   No Windows 7 e posterior, uma opção de menu de atalho pode estar disponível com base no fato de uma condição AQS ser atendida. Para obter mais informações, consulte "obtendo comportamento dinâmico para verbos estáticos usando a sintaxe de consulta avançada" em [criando manipuladores de menu de contexto](../shell/context-menu-handlers.md).
-   As consultas AQS podem ser limitadas a tipos específicos de arquivos, que são conhecidos como tipos de arquivo. Para obter mais informações, consulte [tipos de arquivo e associações](../shell/fa-intro.md). Para obter a documentação de referência de propriedade, consulte [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Usando abordagens SQL e AQS para consultar o índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
