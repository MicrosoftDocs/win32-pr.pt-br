---
description: O MFTrace é uma ferramenta para gerar logs de rastreamento para Microsoft Media Foundation aplicativos.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Usando o MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469963"
---
# <a name="using-mftrace"></a>Usando o MFTrace

O MFTrace é uma ferramenta para gerar logs de rastreamento para Microsoft Media Foundation aplicativos.

O MFTrace usa a biblioteca Detours para conectar-se Media Foundation de API e gerar logs de rastreamento. O MFTrace também pode registrar rastreamentos de qualquer componente que use o ETW (Rastreamento de Eventos para Windows) ou o WPP (pré-processador de rastreamento de software) para gerar rastreamentos. Os logs de rastreamento podem ser gerados iniciando um novo processo do MFTrace ou anexando o MFTrace a um processo existente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]




| Argumentos de linha de comando | Descrição | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>ID do processo ou nome do processo</em><br /> | Anexar a um processo em execução.<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Arquivo de configuração</em><br /> | Ler as configurações do arquivo de configuração especificado. Consulte <a href="mftrace-configuration-file.md">Arquivo de configuração do MFTrace</a>.<br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br /> | Desabilite o rastreamento para processos filho. Por padrão, o rastreamento está habilitado para processos filho.<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | Habilitar símbolos públicos.<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Palavras-chave</em><br /> | Uma lista separada por vírgulas de palavras-chave. Consulte <a href="mftrace-keywords.md">Palavras-chave do MFTrace.</a><br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Nível</em><br /> | O nível de rastreamento.<br /><ul><li>0: nenhum</li><li>1: Crítico</li><li>2: Erro</li><li>3: Aviso</li><li>4: Informativo</li><li>5: Detalhado</li><li>16: Depurar</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Arquivo de saída</em><br /> | Escreva a saída de rastreamento no arquivo especificado. Por padrão, a saída vai para <strong>stdout</strong>.<br /> Se um arquivo de saída for especificado, a extensão de nome de arquivo deverá ser uma das seguintes:<br /><ul><li>.etl: arquivo ETL (log de rastreamento de eventos).</li><li>.log ou .txt: arquivo de texto.</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | Habilitar o modo detalhado.<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | Exibir informações de uso.<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>COMANDO</em><br /> | Argumentos de linha de comando para criar um novo processo.<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | O nome de um arquivo ETL existente. Se esse argumento for fornecido, o arquivo ETL será convertido em saída de texto.<br /> | 




 

## <a name="environment-variables"></a>Variáveis de ambiente

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Para rastrear componentes que usam o WPP (pré-processador de rastreamento de software) do Windows, de definir essa variável de ambiente para especificar o caminho para os arquivos TMF (formato de mensagem de rastreamento) para o componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Se a lookup de símbolo estiver habilitada (**-es**), de definir essa variável de ambiente para especificar o caminho do símbolo.

</dd> </dl>

## <a name="examples"></a>Exemplos

Crie um novo processo e rastreia esse processo:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Anexe o MFTrace a um processo existente:

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

 

Converta um arquivo ETL em um arquivo de texto:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Comentários

Por padrão, o MFTrace gera apenas rastreamentos de Desvios. Para gerar rastreamentos ETW ou WPP, você deve fornecer um arquivo de configuração. O arquivo de configuração fornece os nomes dos provedores de rastreamento. Para obter mais informações, consulte [Arquivo de configuração do MFTrace](mftrace-configuration-file.md).

O MFTrace pode enviar a saída para os seguintes destinos:

-   **stdout** (o padrão).
-   Um arquivo de texto.
-   Um arquivo ETL binário.

Se você estiver registrando rastreamentos ETW/WPP, um arquivo ETL será a opção mais eficiente, pois os dados de rastreamento serão salvos como blobs binários. Depois que a sessão de rastreamento for concluída, você poderá usar o MFTrace para converter o arquivo ETL em um arquivo de texto.

> [!Note]  
> Para rastreamento de desvios, a saída de texto é tão eficiente quanto um arquivo ETL. Portanto, se você registrar somente rastreamentos do Detours (sem rastreamentos ETW/WPP), a saída de texto será recomendada.

 

Para rastreamento de Desvios, você deve anexar o MFTrace a um processo em execução (**-a**) ou usar o MFTrace para criar um novo processo. Para rastreamentos ETW/WPP, o MFTrace escuta qualquer provedor de eventos listado no arquivo de configuração.

Você pode filtrar os resultados do rastreamento especificando palavras-chave de rastreamento, por meio da opção de linha de comando **-k** ou no arquivo de configuração. O uso mais típico, no entanto, é registrar todos os rastreamentos e, em seguida, usar um script ou **grep** para pesquisar padrões de cadeia de caracteres específicos.

## <a name="interpreting-the-trace-results"></a>Interpretando os resultados do rastreamento

Você pode usar o MFTrace para responder a perguntas sobre o que acontece dentro de seu Media Foundation aplicativo ou componente. A tabela a seguir lista algumas perguntas típicas. A segunda coluna fornece a cadeia de caracteres de pesquisa que pode ajudar a responder à pergunta.




| Pergunta | Pesquisar cadeias de caracteres | 
|----------|----------------|
| Ocorreu um erro? | "0xc00d" | 
| A topologia foi resolvida corretamente? | "CTopologyHelpers::Trace" | 
| A sessão de mídia começou? | "MESessionStarted" | 
| Qual arquivo foi tocado? | "CMFSourceResolverDetours" | 
| Quais são os tipos de mídia para os fluxos de origem? | "Novo fluxo", "MENewStream", "CMFMediaSourceDetours::TracePD" | 
| Os fluxos de origem geraram amostras? | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| A reprodução atingiu o final dos dados? | "MEEndOfStream", "MEEndOfPresentation" | 
| O formato mudou? | "MEStreamFormatChanged" (fontes de mídia), "Novo formato", "MESessionStreamSinkFormatChanged" (sinks de mídia) | 
| Quais objetos foram criados? | "COle32ExportDetours:: CoCreateInstance" | 
| As transformações Media Foundation (MFTs) no pipeline processam dados? | "CMFTransformDetours::P rocessOutput", "CMFTransformDetours::P rocessInput" | 
| Quais Estados foram definidos no MFTs? | "CMFTransformDetours::P rocessMessage" | 
| Uma MFT solicitou dados de entrada? | "MF_E_TRANSFORM_NEED_MORE_INPUT" (MFT síncrona), "METransformNeedInput" (MFT assíncrono). | 
| Uma MFT assíncrona produz dados de saída? | "ProcessOutputs disponível" | 
| Houve amostras de solicitação de coletor de mídia? | "MEStreamSinkRequestSample" | 
| Um coletor de mídia recebeu amostras? | "CMFStreamSinkDetours::P rocessSample" | 
| DirectShow: quais exemplos foram processados? | "exemplo", "CMemInputPinDetours" | 
| DirectShow: qual grafo de filtro foi usado? | "CGraphHelpers:: trace" | 
| Houve vários processos? | CreateProcess<blockquote>[!Note]<br />Procure também o identificador do processo, que aparece no início de cada linha de rastreamento.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




