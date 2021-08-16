---
description: A ferramenta de configuração de rastreamento do WinHTTP (Microsoft Windows HTTP Services), WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e de localização de pacotes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7747e0b2fe023ab3c2c86d19a722059482aed19062cf2a450b8d0f237a8b3a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562405"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento

A ferramenta de configuração de rastreamento do [WinHTTP (Microsoft Windows Http Services),](about-winhttp.md) WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e de localização de pacotes. A capacidade de monitorar funções WinHTTP e seu tráfego de rede correspondente é importante. Os aplicativos de depuração que utilizam protocolos de transmissão criptografados, como protocolo SSL (SSL), impedem a interceptação de pacotes na camada de transporte de rede e exigem a capacidade de interceptar o tráfego entre o cliente e o servidor depois que ele for descriptografado. O Microsoft Windows Http Services (WinHTTP) fornece um recurso de rastreamento que tem uma variedade de recursos para interceptar o fluxo de tráfego entre o cliente e o servidor.

Esse recurso de rastreamento pode ser uma ferramenta valiosa para depuração. Ele pode ser usado, por exemplo, para exibir parâmetros passados para várias chamadas de função, bem como para exibir dados reais enviados e recebidos por um aplicativo WinHTTP.

-   [Usando o Recurso de Rastreamento](#using-the-trace-facility)
-   [Interpretando dados de rastreamento](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Usando o Recurso de Rastreamento

O WinHTTP obtém parâmetros de controle de rastreamento do Registro. Esses parâmetros de controle afetam como o WinHTTP produz a saída de rastreamento e como essa saída é formatada. Todos os aplicativos que usam WinHTTP compartilham as mesmas configurações.

Uma ferramenta de configuração de instalação de rastreamento, WinHttpTraceCfg.exe, está disponível como um download no site Windows Ferramentas do Kit de Recursos [do Windows Server 2003.](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) A ferramenta de configuração define ou recupera as configurações do registro do recurso de rastreamento com base nos parâmetros de linha de comando especificados.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

A tabela a seguir lista os possíveis parâmetros para a ferramenta de configuração.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<p><<em>prefixo</em> > -< <em>nome do aplicativo</em> > . <hora <em></em> > .log</p>
<p>Se um prefixo não for especificado, uma cadeia de caracteres vazia será usada. &quot; * &quot; Especifique para excluir um prefixo existente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Especifica se a saída do rastreamento é exibida em um depurador ou gravado em um arquivo.</p>

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
<td>Exibe apenas cabeçalhos HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Configuração padrão. Mostra o tráfego de rede American National Standards Institute formato ANSI.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Mostra o tráfego de rede em formato hexadecimal.</td>
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
<td>Configuração padrão. Chamadas de função não são registradas.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Chamadas de função de nível superior são registradas.</td>
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



 

Executar a ferramenta de configuração do recurso de rastreamento e especificar nenhum parâmetro recupera e exibe as configurações atuais do Registro.

> [!Note]  
> Os arquivos de log crescem rapidamente e degradam o desempenho do aplicativo. Verifique se o espaço necessário da unidade de disco rígido está disponível antes de habilenciar o recurso de rastreamento.

 

## <a name="interpreting-trace-data"></a>Interpretando dados de rastreamento

O fluxo de dados do recurso de rastreamento reflete as funções WinHTTP chamadas no aplicativo e quaisquer dados HTTP enviados ou recebidos. Em alguns casos, as funções chamadas internamente pelo WinHTTP também são mostradas.

A imagem a seguir mostra uma parte de um arquivo de log gerado pelo recurso de rastreamento. Vários itens são realçadas e rotuladas.

![rastreamento de exemplo](images/ss-tracer-wco.png)

Cada linha de saída de rastreamento contém informações em três colunas. A primeira coluna mostra a data e a hora em que a entrada foi registrada. A segunda coluna mostra um ID (identificador de solicitação) que pode ser usado para diferenciar entre várias solicitações. Se a entrada de log não corresponder a uma solicitação específica, " \* Sessão " será exibido nesta \* coluna. Pode ser útil classificar o arquivo de log com base nessa ID para ver apenas os eventos que ocorrem para uma única solicitação. O exemplo a seguir mostra um comando que você pode usar para classificar o arquivo de log.

**findstr 00000001 LogFile.log**

A terceira coluna mostra uma chamada de função, tráfego HTTP ou uma mensagem de status incluída para ajudar a interpretar o rastreamento.

Quando uma entrada de log corresponde a uma chamada de função, os parâmetros da função também são registrados. Os endereços de memória são exibidos em hexadecimal, enquanto todos os outros valores são exibidos como uma cadeia de caracteres ASCII. O recurso de rastreamento também registra o tempo de retorno e o valor de cada função.

O formato dos dados HTTP depende das configurações do Registro especificadas com a ferramenta de configuração do recurso de rastreamento. Quando os dados HTTP são criptografados, os dados descriptografados também são mostrados na saída de rastreamento.

 

 




