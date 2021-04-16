---
description: As funções nesta seção instalam e configuram drivers de impressora em um computador.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Referência de instalação do driver de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772542"
---
# <a name="printer-driver-installation-reference"></a>Referência de instalação do driver de impressora

As funções nesta seção instalam e configuram drivers de impressora em um computador.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="addmonitor.md"><strong>Addmonitor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addmonitor"><strong>addmonitor</strong></a> instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> adiciona o nome de uma porta à lista de portas com suporte. A função <strong>AddPort</strong> é exportada pelo monitor de porta.<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.<br/> Para obter mais flexibilidade na instalação ou atualização de drivers de impressora, use a função <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> porque ela permite a atualização estrita, o downgrade estrito, a cópia somente de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).<br/>
<blockquote>
[!Note]<br />
A instalação de um driver de impressora sem um pacote de driver não é mais recomendada. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver. Além de ter os recursos do <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, ele também tem opções que permitem a atualização estrita, o downgrade estrito, a cópia de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).<br/>
<blockquote>
[!Note]<br />
A instalação de um driver de impressora sem um pacote de driver não é mais recomendada. Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> remove um monitor de porta adicionado pela função <a href="addmonitor.md"><strong>addmonitor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>DeletePort</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> exibe uma caixa de diálogo que permite ao usuário excluir um nome de porta.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.<br/> Para excluir os arquivos associados ao driver, além de remover o nome de driver de impressora especificado da lista de nomes de drivers com suporte para um servidor, use a função <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .<br/> <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> excluirá um driver somente se nenhuma versão do driver estiver em uso para o ambiente especificado. <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> pode excluir versões específicas do driver.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver. Essa função também pode excluir versões específicas do driver.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br/></td>
<td>Exclui um pacote de driver de impressora do repositório de drivers.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> remove um processador de impressão adicionado pela função <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> remove um provedor de impressão adicionado pela função <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>EnumMonitors</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera informações sobre os monitores de porta instalados no servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera as portas que estão disponíveis para impressão em um servidor especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera os drivers de impressora instalados em um servidor de impressora especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera os processadores de impressão instalados no servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br/></td>
<td>Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o <strong>GetPrinterDriver</strong> o instalará.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td>A função <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o <strong>GetPrinterDriver2</strong> o instalará e exibirá qualquer interface do usuário na janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> recupera o caminho do diretório do driver de impressora.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br/></td>
<td>Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br/></td>
<td>A função <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> recupera o caminho para o diretório do processador de impressão no servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br/></td>
<td>Instala um driver de impressora de um pacote de driver que está no repositório de drivers do servidor de impressão.<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br/></td>
<td>Carrega um driver de impressora no repositório de drivers do servidor de impressão para que ele possa ser instalado chamando <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

