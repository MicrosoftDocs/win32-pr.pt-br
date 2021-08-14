---
description: MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Microsoft Media Foundation.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Usando MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03cb19f17978236b3e4edd8415f524913c90d99d7a7caf4183dd885d340cfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737319"
---
# <a name="using-mftrace"></a>Usando MFTrace

MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Microsoft Media Foundation.

O MFTrace usa a biblioteca de desvios para conectar Media Foundation chamadas à API e gerar logs de rastreamento. o MFTrace também pode registrar rastreamentos de qualquer componente que usa o rastreamento de eventos para Windows (ETW) ou o WPP (pré-processador de rastreamento de software) para gerar rastreamentos. Os logs de rastreamento podem ser gerados iniciando um novo processo do MFTrace ou anexando MFTrace a um processo existente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** do *processo* \] \[ **-c** *configuração*- \] \[ **DC**- \] \[ **es** \] \[ **-k** -palavras- *chave* \] \[ **-l** *nível* \] \[ **-o** de *saída* \] \[ **-v** \] \[ **-?** \] \[ {*Comando* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argumentos de linha de comando</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>ID do processo ou nome do processo</em><br/></td>
<td>Anexar a um processo em execução.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Arquivo de configuração</em><br/></td>
<td>Ler as configurações do arquivo de configuração especificado. Consulte o <a href="mftrace-configuration-file.md">arquivo de configuração MFTrace</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br/></td>
<td>Desabilitar o rastreamento de processos filho. Por padrão, o rastreamento está habilitado para processos filho.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Habilitar símbolos públicos.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Palavras-chave</em><br/></td>
<td>Uma lista separada por vírgulas de palavras-chave. Consulte <a href="mftrace-keywords.md">palavras-chave MFTrace</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Nível</em> do<br/></td>
<td>O nível de rastreamento.<br/>
<ul>
<li>0: nenhum</li>
<li>1: crítico</li>
<li>2: erro</li>
<li>3: aviso</li>
<li>4: informativo</li>
<li>5: detalhado</li>
<li>16: Depurar</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Arquivo de saída</em><br/></td>
<td>Grave a saída de rastreamento no arquivo especificado. Por padrão, a saída vai para <strong>stdout</strong>.<br/> Se um arquivo de saída for especificado, a extensão de nome de arquivo deverá ser uma das seguintes:<br/>
<ul>
<li>. etl: arquivo de log de rastreamento de eventos (ETL).</li>
<li>. log ou .txt: arquivo de texto.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Habilite o modo detalhado.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Exibir informações de uso.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>LINHA</em><br/></td>
<td>Argumentos de linha de comando para criar um novo processo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>O nome de um arquivo ETL existente. Se esse argumento for fornecido, o arquivo ETL será convertido em saída de texto.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Variáveis de ambiente

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

para rastrear os componentes que usam o Windows WPP (pré-processador de rastreamento de software), defina essa variável de ambiente para especificar o caminho para os arquivos de formato de mensagem de rastreamento (TMF) para o componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Se a pesquisa de símbolos estiver habilitada (**-es**), defina essa variável de ambiente para especificar o caminho do símbolo.

</dd> </dl>

## <a name="examples"></a>Exemplos

Crie um novo processo e rastreie esse processo:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Anexar MFTrace a um processo existente:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Enviar saída de rastreamento para um arquivo de texto:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Rastrear eventos ETW ou WPP:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> O primeiro exemplo gera um arquivo de texto. O segundo exemplo gera um arquivo ETL.

 

Converter um arquivo ETL em um arquivo de texto:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Comentários

Por padrão, MFTrace gera apenas rastreamentos de desvios. Para gerar rastreamentos ETW ou WPP, você deve fornecer um arquivo de configuração. O arquivo de configuração fornece os nomes dos provedores de rastreamento. Para obter mais informações, consulte [MFTrace Configuration File](mftrace-configuration-file.md).

MFTrace pode enviar a saída para os seguintes destinos:

-   **stdout** (o padrão).
-   Um arquivo de texto.
-   Um arquivo ETL binário.

Se você estiver registrando rastreamentos ETW/WPP, um arquivo ETL será a opção mais eficiente, porque os dados de rastreamento são salvos como blobs binários. Depois que a sessão de rastreamento for concluída, você poderá usar MFTrace para converter o arquivo ETL em um arquivo de texto.

> [!Note]  
> Para rastreamento de desvios, a saída de texto é tão eficiente quanto um arquivo ETL. Portanto, se você registrar apenas rastreamentos de desvios (sem rastreamentos de ETW/WPP), a saída de texto será recomendada.

 

Para rastreamento de desvios, você deve anexar MFTrace a um processo em execução (**-a**) ou usar MFTrace para criar um novo processo. Para rastreamentos de ETW/WPP, o MFTrace escuta qualquer provedor de eventos listado no arquivo de configuração.

Você pode filtrar os resultados do rastreamento especificando palavras-chave de rastreamento, seja por meio da opção de linha de comando **-k** ou no arquivo de configuração. O uso mais comum, no entanto, é registrar em log todos os rastreamentos e, em seguida, usar um script ou **grep** para Pesquisar padrões de cadeia de caracteres específicos.

## <a name="interpreting-the-trace-results"></a>Interpretando os resultados do rastreamento

Você pode usar o MFTrace para responder a perguntas sobre o que acontece dentro de seu aplicativo Media Foundation ou componente. A tabela a seguir lista algumas perguntas típicas. A segunda coluna fornece a cadeia de caracteres de pesquisa que pode ajudar a responder à pergunta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pergunta</th>
<th>Pesquisar cadeias de caracteres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ocorreu um erro?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>A topologia foi resolvida corretamente?</td>
<td>&quot;CTopologyHelpers:: Trace&quot;</td>
</tr>
<tr class="odd">
<td>A sessão de mídia foi iniciada?</td>
<td>&quot;MESessionStarted&quot;</td>
</tr>
<tr class="even">
<td>Qual arquivo foi reproduzido?</td>
<td>&quot;CMFSourceResolverDetours&quot;</td>
</tr>
<tr class="odd">
<td>Quais são os tipos de mídia para os fluxos de origem?</td>
<td>&quot;Novo fluxo &quot; , &quot; MENewStream &quot; , &quot; CMFMediaSourceDetours:: TracePD&quot;</td>
</tr>
<tr class="even">
<td>Os fluxos de origem geram amostras?</td>
<td>&quot;CMFMediaStreamDetours:: HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>A reprodução chegou ao fim dos dados?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>O formato foi alterado?</td>
<td>&quot;MEStreamFormatChanged &quot; (fontes de mídia), &quot; novo formato &quot; , &quot; MESessionStreamSinkFormatChanged &quot; (coletores de mídia)</td>
</tr>
<tr class="odd">
<td>Quais objetos foram criados?</td>
<td>&quot;COle32ExportDetours::CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>As MFTs (Media Foundation de dados) no pipeline processaram dados?</td>
<td>&quot;CMFTransformDetours::P rocessOutput, &quot; &quot; CMFTransformDetours::P rocessInput&quot;</td>
</tr>
<tr class="odd">
<td>Quais estados foram definidos nos MFTs?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>Uma solicitação MFT solicitou dados de entrada?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (MFT síncrono), &quot; METransformNeedInput &quot; (MFT assíncrono).</td>
</tr>
<tr class="odd">
<td>Uma MFT assíncrona produziu dados de saída?</td>
<td>&quot;ProcessOutputs disponíveis&quot;</td>
</tr>
<tr class="even">
<td>Um sink de mídia solicitou exemplos?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>Um sink de mídia recebeu exemplos?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: Quais exemplos foram processados?</td>
<td>&quot;sample &quot; , &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: qual grafo de filtro foi usado?</td>
<td>&quot;CGraphHelpers::Trace&quot;</td>
</tr>
<tr class="even">
<td>Havia vários processos?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Procure também o identificador do processo, que aparece no início de cada linha de rastreamento.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




