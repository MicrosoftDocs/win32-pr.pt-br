---
description: a ferramenta de configuração de rastreamento do Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e detecção de pacotes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e292373c0da19be32f48d7f62f558953406e8d1b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622562"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento

a ferramenta de configuração de rastreamento do [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e detecção de pacotes. A capacidade de monitorar as funções WinHTTP e seu tráfego de rede correspondente é importante. Depurar aplicativos que utilizam protocolos de transmissão criptografada, como protocolo SSL (SSL), impedir a detecção de pacotes na camada de transporte de rede e exigir a capacidade de interceptar o tráfego entre o cliente e o servidor depois que ele tiver sido descriptografado. o Microsoft Windows HTTP Services (WinHTTP) fornece um recurso de rastreamento que tem uma variedade de recursos para interceptar o fluxo de tráfego entre o cliente e o servidor.

Esse recurso de rastreamento pode ser uma ferramenta valiosa para depuração. Ele pode ser usado, por exemplo, para exibir parâmetros passados para várias chamadas de função, bem como para exibir dados reais enviados e recebidos por um aplicativo WinHTTP.

-   [Usando o recurso de rastreamento](#using-the-trace-facility)
-   [Interpretando dados de rastreamento](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Usando o recurso de rastreamento

O WinHTTP Obtém os parâmetros de controle de rastreamento do registro. Esses parâmetros de controle afetam como o WinHTTP produz a saída de rastreamento e como essa saída é formatada. Todos os aplicativos que usam WinHTTP compartilham as mesmas configurações.

uma ferramenta de configuração de recurso de rastreamento, WinHttpTraceCfg.exe, está disponível como um download no site de [ferramentas do Kit de recursos do Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . A ferramenta de configuração define ou recupera as configurações do registro de recurso de rastreamento com base nos parâmetros de linha de comando especificados.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

A tabela a seguir lista os possíveis parâmetros para a ferramenta de configuração do.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Exibe dados de sintaxe.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Especifica se o recurso de rastreamento está habilitado ou desabilitado. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuração padrão. Desabilita o rastreamento.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita o rastreamento.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>Especifica um prefixo para o arquivo de log. O prefixo pode incluir um caminho. O arquivo de log é gravado no diretório atual ou no diretório especificado no prefixo e tem o formato a seguir.</p>
<p><<em></em> > prefixo -< <em>nome do aplicativo</em> > . <em>Tempo</em>de <> . log</p>
<p>Se um prefixo não for especificado, uma cadeia de caracteres vazia será usada. Especifique &quot; * &quot; para excluir um prefixo existente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Especifica se a saída do rastreamento é exibida em um depurador ou gravada em um arquivo.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuração padrão. Grava no arquivo de log.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Exibe em um depurador.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>Especifica como o tráfego de rede (solicitações e respostas) é exibido.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Exibe somente cabeçalhos HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Configuração padrão. Mostra o tráfego de rede no formato American National Standards Institute (ANSI).</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Mostra o tráfego de rede no formato hexadecimal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-T</td>
<td><p>Especifica se as chamadas de função de nível superior são registradas no rastreamento.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuração padrão. As chamadas de função não são registradas.</td>
</tr>
<tr class="even">
<td>1</td>
<td>As chamadas de função de nível superior são registradas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>Especifica o tamanho máximo, em bytes, de um arquivo de log gerado pelo recurso de rastreamento. Se essa opção for especificada sem um tamanho, o valor mínimo será 65.535 bytes. Se um arquivo de log atingir o tamanho máximo, o conteúdo do arquivo será apagado. Os dados de rastreamento continuam a ser gravados no arquivo de log.</p></td>
</tr>
</tbody>
</table>



 

A execução da ferramenta de configuração de recurso de rastreamento e a especificação de nenhum parâmetro recupera e exibe as configurações atuais do registro.

> [!Note]  
> Os arquivos de log crescem rapidamente e prejudicam o desempenho do aplicativo. Verifique se o espaço necessário na unidade de disco rígido está disponível antes de habilitar o recurso de rastreamento.

 

## <a name="interpreting-trace-data"></a>Interpretando dados de rastreamento

O fluxo de dados de recursos de rastreamento reflete as funções de WinHTTP chamadas no aplicativo e todos os dados HTTP enviados ou recebidos. Em alguns casos, as funções chamadas internamente pelo WinHTTP também são mostradas.

A imagem a seguir mostra uma parte de um arquivo de log gerado pelo recurso de rastreamento. Vários itens são realçados e rotulados.

![rastreamento de exemplo](images/ss-tracer-wco.png)

Cada linha da saída de rastreamento contém informações em três colunas. A primeira coluna mostra a data e a hora em que a entrada foi registrada. A segunda coluna mostra um identificador de solicitação (ID) que pode ser usado para diferenciar entre várias solicitações. Se a entrada de log não corresponder a uma solicitação específica, " \* sessão \* " será exibida nesta coluna. Pode ser útil classificar o arquivo de log com base nessa ID para ver apenas os eventos que ocorrem para uma única solicitação. O exemplo a seguir mostra um comando que você pode usar para classificar o arquivo de log.

**findstr 00000001 LogFile. log**

A terceira coluna mostra uma chamada de função, um tráfego HTTP ou uma mensagem de status incluída para ajudar a interpretar o rastreamento.

Quando uma entrada de log corresponde a uma chamada de função, os parâmetros da função também são registrados. Os endereços de memória são exibidos em hexadecimal, enquanto todos os outros valores são exibidos como uma cadeia de caracteres ASCII. O recurso de rastreamento também registra a hora de retorno e o valor de cada função.

O formato dos dados HTTP depende das configurações do registro especificadas com a ferramenta de configuração do recurso de rastreamento. Quando os dados HTTP são criptografados, os dados descriptografados também são mostrados na saída do rastreamento.

 

 




