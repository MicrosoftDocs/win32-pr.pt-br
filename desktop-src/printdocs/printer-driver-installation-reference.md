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
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="800af-103">Referência de instalação do driver de impressora</span><span class="sxs-lookup"><span data-stu-id="800af-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="800af-104">As funções nesta seção instalam e configuram drivers de impressora em um computador.</span><span class="sxs-lookup"><span data-stu-id="800af-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="800af-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="800af-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="800af-106">Função</span><span class="sxs-lookup"><span data-stu-id="800af-106">Function</span></span></th>
<th><span data-ttu-id="800af-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="800af-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="800af-108"><a href="addmonitor.md"><strong>Addmonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-109">A função <a href="/windows/desktop/printdocs/addmonitor"><strong>addmonitor</strong></a> instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="800af-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-111">A função <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> adiciona o nome de uma porta à lista de portas com suporte.</span><span class="sxs-lookup"><span data-stu-id="800af-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="800af-112">A função <strong>AddPort</strong> é exportada pelo monitor de porta.</span><span class="sxs-lookup"><span data-stu-id="800af-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-114">A função <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="800af-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="800af-115">Para obter mais flexibilidade na instalação ou atualização de drivers de impressora, use a função <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> porque ela permite a atualização estrita, o downgrade estrito, a cópia somente de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).</span><span class="sxs-lookup"><span data-stu-id="800af-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="800af-116">A instalação de um driver de impressora sem um pacote de driver não é mais recomendada.</span><span class="sxs-lookup"><span data-stu-id="800af-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="800af-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> em vez disso.</span><span class="sxs-lookup"><span data-stu-id="800af-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-119">A função <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="800af-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="800af-120">Além de ter os recursos do <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, ele também tem opções que permitem a atualização estrita, o downgrade estrito, a cópia de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).</span><span class="sxs-lookup"><span data-stu-id="800af-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="800af-121">A instalação de um driver de impressora sem um pacote de driver não é mais recomendada.</span><span class="sxs-lookup"><span data-stu-id="800af-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="800af-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> em vez disso.</span><span class="sxs-lookup"><span data-stu-id="800af-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-124">A função <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.</span><span class="sxs-lookup"><span data-stu-id="800af-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-126">A função <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.</span><span class="sxs-lookup"><span data-stu-id="800af-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-128">A função <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.</span><span class="sxs-lookup"><span data-stu-id="800af-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-130">A função <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> remove um monitor de porta adicionado pela função <a href="addmonitor.md"><strong>addmonitor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="800af-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-132">A função <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> exibe uma caixa de diálogo que permite ao usuário excluir um nome de porta.</span><span class="sxs-lookup"><span data-stu-id="800af-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-134">A função <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.</span><span class="sxs-lookup"><span data-stu-id="800af-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="800af-135">Para excluir os arquivos associados ao driver, além de remover o nome de driver de impressora especificado da lista de nomes de drivers com suporte para um servidor, use a função <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="800af-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="800af-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> excluirá um driver somente se nenhuma versão do driver estiver em uso para o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="800af-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> pode excluir versões específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="800af-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-139">A função <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver.</span><span class="sxs-lookup"><span data-stu-id="800af-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="800af-140">Essa função também pode excluir versões específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="800af-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-142">Exclui um pacote de driver de impressora do repositório de drivers.</span><span class="sxs-lookup"><span data-stu-id="800af-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-144">A função <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> remove um processador de impressão adicionado pela função <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="800af-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-146">A função <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> remove um provedor de impressão adicionado pela função <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="800af-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-148">A função <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera informações sobre os monitores de porta instalados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-150">A função <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera as portas que estão disponíveis para impressão em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-152">A função <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera os drivers de impressora instalados em um servidor de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-154">A função <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.</span><span class="sxs-lookup"><span data-stu-id="800af-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-156">A função <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera os processadores de impressão instalados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-158">Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.</span><span class="sxs-lookup"><span data-stu-id="800af-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-160">A função <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera dados de driver para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="800af-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="800af-161">Se o driver não estiver instalado no computador local, o <strong>GetPrinterDriver</strong> o instalará.</span><span class="sxs-lookup"><span data-stu-id="800af-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-163">A função <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera dados de driver para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="800af-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="800af-164">Se o driver não estiver instalado no computador local, o <strong>GetPrinterDriver2</strong> o instalará e exibirá qualquer interface do usuário na janela especificada.</span><span class="sxs-lookup"><span data-stu-id="800af-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-166">A função <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> recupera o caminho do diretório do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="800af-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-168">Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="800af-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-170">A função <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> recupera o caminho para o diretório do processador de impressão no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="800af-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="800af-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-172">Instala um driver de impressora de um pacote de driver que está no repositório de drivers do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="800af-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="800af-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="800af-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="800af-174">Carrega um driver de impressora no repositório de drivers do servidor de impressão para que ele possa ser instalado chamando <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="800af-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

