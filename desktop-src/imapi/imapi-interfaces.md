---
title: Interfaces IMAPi
description: As tabelas a seguir identificam e descrevem brevemente as interfaces usadas pelos desenvolvedores C/C++ e o objeto de script associado. Prefixe o nome do objeto na tabela com \ 0034; IMAPI2. \ 0034; para qualificar totalmente o nome do objeto ao criar o objeto no script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105792658"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="88579-105">Interfaces IMAPi</span><span class="sxs-lookup"><span data-stu-id="88579-105">IMAPI Interfaces</span></span>

<span data-ttu-id="88579-106">As tabelas a seguir identificam e descrevem brevemente as interfaces usadas pelos desenvolvedores C/C++ e o objeto de script associado.</span><span class="sxs-lookup"><span data-stu-id="88579-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="88579-107">Prefixe o nome do objeto na tabela com "IMAPI2".</span><span class="sxs-lookup"><span data-stu-id="88579-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="88579-108">para qualificar totalmente o nome do objeto ao criar o objeto no script.</span><span class="sxs-lookup"><span data-stu-id="88579-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="88579-109">A tabela a seguir lista as interfaces associadas aos dispositivos, ao mecanismo de gravação e ao formato gravadores e borracha.</span><span class="sxs-lookup"><span data-stu-id="88579-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88579-110">Interface</span><span class="sxs-lookup"><span data-stu-id="88579-110">Interface</span></span></td>
<td><span data-ttu-id="88579-111">Objeto</span><span class="sxs-lookup"><span data-stu-id="88579-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-112">Mecanismo de gravação de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="88579-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="88579-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="88579-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="88579-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="88579-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-117">Gravador de imagem principal.</span><span class="sxs-lookup"><span data-stu-id="88579-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="88579-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="88579-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="88579-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-122">Borracha de disco.</span><span class="sxs-lookup"><span data-stu-id="88579-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="88579-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="88579-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-126">Gravador de imagem bruto.</span><span class="sxs-lookup"><span data-stu-id="88579-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="88579-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="88579-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="88579-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-131">Gravador de imagem de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="88579-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="88579-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="88579-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="88579-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-136">Enumeração de dispositivos de disco na lista de hardware do sistema.</span><span class="sxs-lookup"><span data-stu-id="88579-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="88579-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="88579-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-139">Delegado de notificação para o objeto MsftDiscMaster2.</span><span class="sxs-lookup"><span data-stu-id="88579-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="88579-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="88579-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-142">Dispositivo de gravação individual.</span><span class="sxs-lookup"><span data-stu-id="88579-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="88579-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="88579-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="88579-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-146">Atributos de gravação de dispositivo, incluindo o tipo de mídia, a velocidade de gravação e o tipo de controle de velocidade angular.</span><span class="sxs-lookup"><span data-stu-id="88579-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="88579-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-148">MsftWriteSpeedDescriptor</span><span class="sxs-lookup"><span data-stu-id="88579-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88579-149">A tabela a seguir lista as interfaces do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88579-150">Interface</span><span class="sxs-lookup"><span data-stu-id="88579-150">Interface</span></span></td>
<td><span data-ttu-id="88579-151">Objeto</span><span class="sxs-lookup"><span data-stu-id="88579-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-152">Fluxo de imagem de inicialização e propriedades para integrar a imagem inicializável na imagem do disco.</span><span class="sxs-lookup"><span data-stu-id="88579-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="88579-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-154">Bootoptions</span><span class="sxs-lookup"><span data-stu-id="88579-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-155">Imagem e propriedades do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-155">File system image and properties.</span></span> <span data-ttu-id="88579-156">Esse objeto inclui todas as faixas e referências à imagem de inicialização e à imagem de resultado.</span><span class="sxs-lookup"><span data-stu-id="88579-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="88579-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="88579-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="88579-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="88579-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-162">CFileSystemImage</span><span class="sxs-lookup"><span data-stu-id="88579-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-163">Contêiner do fluxo de dados fornecido pelo objeto do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="88579-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-165">FileSystemImageResult</span><span class="sxs-lookup"><span data-stu-id="88579-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-166">Item de diretório na imagem do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="88579-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="88579-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-169">FsiDirectoryItem</span><span class="sxs-lookup"><span data-stu-id="88579-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-170">Item de arquivo na imagem do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="88579-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="88579-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-173">FsiFileItem</span><span class="sxs-lookup"><span data-stu-id="88579-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-174">Interface que contém as propriedades comuns aos itens de arquivo e diretório.</span><span class="sxs-lookup"><span data-stu-id="88579-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="88579-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-176">FsiItem</span><span class="sxs-lookup"><span data-stu-id="88579-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-177">Criação de imagem de CD bruta.</span><span class="sxs-lookup"><span data-stu-id="88579-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="88579-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="88579-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-180">MsftRawCDImageCreator</span><span class="sxs-lookup"><span data-stu-id="88579-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-181">Objeto do auxiliar de objeto de fluxo para concatenar vários fluxos.</span><span class="sxs-lookup"><span data-stu-id="88579-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="88579-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-183">MsftStreamConcatenate</span><span class="sxs-lookup"><span data-stu-id="88579-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-184">Fluxo intercalado para adicionar à imagem do disco.</span><span class="sxs-lookup"><span data-stu-id="88579-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="88579-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-186">MsftStreamInterleave</span><span class="sxs-lookup"><span data-stu-id="88579-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-187">Fluxo gerado por pseudo-aleatório.</span><span class="sxs-lookup"><span data-stu-id="88579-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="88579-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="88579-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-190">O objeto de script <strong>MsftStreamZero</strong> não é implementado como uma interface.</span><span class="sxs-lookup"><span data-stu-id="88579-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="88579-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88579-192">A tabela a seguir lista as interfaces auxiliares.</span><span class="sxs-lookup"><span data-stu-id="88579-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88579-193">Interface</span><span class="sxs-lookup"><span data-stu-id="88579-193">Interface</span></span></td>
<td><span data-ttu-id="88579-194">Objeto</span><span class="sxs-lookup"><span data-stu-id="88579-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-195">Coleção de intervalos de setor em uma imagem do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="88579-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="88579-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="88579-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-198">Nenhum objeto correspondente</span><span class="sxs-lookup"><span data-stu-id="88579-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-199">Suporte à verificação de gravação.</span><span class="sxs-lookup"><span data-stu-id="88579-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="88579-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-201">Nenhum objeto correspondente</span><span class="sxs-lookup"><span data-stu-id="88579-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-202">Enumerador de FsiItems para aplicativos C/C++.</span><span class="sxs-lookup"><span data-stu-id="88579-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="88579-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-204">EnumFsiItems</span><span class="sxs-lookup"><span data-stu-id="88579-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-205">Enumerador de ProgressItems para aplicativos C/C++.</span><span class="sxs-lookup"><span data-stu-id="88579-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="88579-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-207">EnumProgressItems</span><span class="sxs-lookup"><span data-stu-id="88579-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="88579-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="88579-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-210">suporte à verificação de imagem. ISO.</span><span class="sxs-lookup"><span data-stu-id="88579-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="88579-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-212">Nenhum objeto correspondente</span><span class="sxs-lookup"><span data-stu-id="88579-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-213">Suporte a várias sessões.</span><span class="sxs-lookup"><span data-stu-id="88579-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="88579-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-215">Nenhum objeto correspondente</span><span class="sxs-lookup"><span data-stu-id="88579-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-216">Suporte sequencial de várias sessões.</span><span class="sxs-lookup"><span data-stu-id="88579-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="88579-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="88579-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-219">MsftMultisessionSequential</span><span class="sxs-lookup"><span data-stu-id="88579-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88579-220">Nome do arquivo e blocos associados na imagem do resultado.</span><span class="sxs-lookup"><span data-stu-id="88579-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="88579-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-222">ProgressItem</span><span class="sxs-lookup"><span data-stu-id="88579-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88579-223">Lista de imagens de resultado, dividida por nome de arquivo e blocos associados.</span><span class="sxs-lookup"><span data-stu-id="88579-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="88579-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="88579-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="88579-225">ProgressItems</span><span class="sxs-lookup"><span data-stu-id="88579-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




