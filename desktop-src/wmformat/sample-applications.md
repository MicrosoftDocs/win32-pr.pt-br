---
title: Aplicativos de exemplo do SDK do Windows Media Format
description: Aplicativos de exemplo do SDK do Windows Media Format
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- SDK do Windows Media Format, aplicativos de exemplo
- DRM (gerenciamento de direitos digitais), aplicativos de exemplo
- DRM (gerenciamento de direitos digitais), aplicativos de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454530"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="72f32-106">Aplicativos de exemplo do SDK do Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="72f32-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="72f32-107">O código de exemplo fornecido com esse SDK está na forma de projetos para Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="72f32-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="72f32-108">A maioria dos exemplos está em C++, mas ManagedWMFSDKWrapper e ManagedMetadataEdit exigem C#.</span><span class="sxs-lookup"><span data-stu-id="72f32-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="72f32-109">Esses exemplos não funcionarão a menos que o Windows Media Format SDK ou o SDK do Windows Player tenha sido instalado.</span><span class="sxs-lookup"><span data-stu-id="72f32-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="72f32-110">As informações de uso de cada exemplo estão contidas em um arquivo de readme.txt em cada diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="72f32-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72f32-111">Samle</span><span class="sxs-lookup"><span data-stu-id="72f32-111">Samle</span></span></th>
<th><span data-ttu-id="72f32-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="72f32-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72f32-113">AudioPlayer</span><span class="sxs-lookup"><span data-stu-id="72f32-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="72f32-114">Reproduz arquivos de mídia do Windows, incluindo arquivos protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="72f32-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="72f32-115">Ele é controlado por meio de uma GUI, e os comandos incluem reproduzir, pausar, buscar e parar.</span><span class="sxs-lookup"><span data-stu-id="72f32-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="72f32-116">Ele pode reproduzir arquivos locais ou arquivos lidos da Internet (incluindo as saídas para a Internet usando o exemplo WMVNetWrite).</span><span class="sxs-lookup"><span data-stu-id="72f32-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72f32-117">As partes de DRM deste exemplo não têm suporte em versões baseadas em x64 do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f32-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-118">DRMHeader</span><span class="sxs-lookup"><span data-stu-id="72f32-118">DRMHeader</span></span></td>
<td><span data-ttu-id="72f32-119">DRMHeader é um aplicativo de console que usa a interface <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> do editor de metadados para ler atributos DRM de arquivos sem vincular à biblioteca estática do DRM.</span><span class="sxs-lookup"><span data-stu-id="72f32-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72f32-120">Não há suporte para este exemplo em versões baseadas em x64 do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f32-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-121">DRMShow</span><span class="sxs-lookup"><span data-stu-id="72f32-121">DRMShow</span></span></td>
<td><span data-ttu-id="72f32-122">DRMShow é um aplicativo de console que mostra como ler as propriedades de <a href="wmformat-glossary.md"><em>DRM</em></a> de um arquivo de mídia do Windows usando o método <strong>IWMDRMReader:: GetDRMProperty</strong> . Este exemplo demonstra o uso do método <strong>IWMDRMReader:: GetDRMProperty</strong> e as propriedades que podem ser recuperadas do leitor de DRM.</span><span class="sxs-lookup"><span data-stu-id="72f32-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="72f32-123">Ele não demonstra como adquirir uma licença para conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="72f32-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="72f32-124">Este exemplo requer que a biblioteca de stub de DRM WMStubDRM. lib seja compilada.</span><span class="sxs-lookup"><span data-stu-id="72f32-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="72f32-125">Não há suporte para este exemplo em versões baseadas em x64 do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f32-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="72f32-126">Ao adquirir o WMStubDRM. lib da Microsoft, o nível de segurança do aplicativo é atribuído à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="72f32-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="72f32-127">Se o nível de segurança da biblioteca que você recebe não for suficiente para reproduzir um arquivo protegido, este exemplo exibirá um erro.</span><span class="sxs-lookup"><span data-stu-id="72f32-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-128">DirectShowInterop/DSCopy</span><span class="sxs-lookup"><span data-stu-id="72f32-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="72f32-129">Transcodifica um ou mais arquivos em um arquivo ASF usando o filtro de gravador ASF do DirectShow WM.</span><span class="sxs-lookup"><span data-stu-id="72f32-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="72f32-130">O arquivo de entrada pode ser qualquer formato compactado ou descompactado com suporte do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72f32-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-131">DirectShowInterop/DSPlay</span><span class="sxs-lookup"><span data-stu-id="72f32-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="72f32-132">Este exemplo é um player de arquivo de mídia de áudio/vídeo interativo com suporte a <a href="wmformat-glossary.md"><em>DRM</em></a> .</span><span class="sxs-lookup"><span data-stu-id="72f32-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="72f32-133">Ele usa o filtro de leitor ASF do WM do DirectShow para reproduzir arquivos de mídia do Windows (ASF, WMA, WMV) sem proteção DRM e arquivos que usam DRM em um nível de 100 ou abaixo.</span><span class="sxs-lookup"><span data-stu-id="72f32-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="72f32-134">Consulte readme.txt no diretório da amostra para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="72f32-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-135">DirectShowInterop/DSSeekFm</span><span class="sxs-lookup"><span data-stu-id="72f32-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="72f32-136">Este exemplo demonstra como usar o filtro de leitor ASF do DirectShow WM para reproduzir conteúdo ASF em um grafo de filtro do DirectShow e também como usar o suporte à busca de quadros no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="72f32-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-137">Gerenciado/WMFSDKWrapper</span><span class="sxs-lookup"><span data-stu-id="72f32-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="72f32-138">Esse assembly gerenciado serve como um wrapper usado por exemplos de código gerenciado para acessar algumas interfaces de metadados deste SDK.</span><span class="sxs-lookup"><span data-stu-id="72f32-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-139">Gerenciado/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="72f32-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="72f32-140">Esse aplicativo C# pode ser usado para exibir e editar metadados de arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f32-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="72f32-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="72f32-142">Esta é uma versão em C++ do aplicativo MetadataEdit gerenciado.</span><span class="sxs-lookup"><span data-stu-id="72f32-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-143">ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="72f32-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="72f32-144">Este exemplo de aplicativo de console mostra como ler dados de <strong>IStream</strong> com WMReader.</span><span class="sxs-lookup"><span data-stu-id="72f32-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="72f32-145">A origem <strong>IStream</strong> foi implementada para usar um arquivo no formato Windows Media (WMA/WMV/ASF).</span><span class="sxs-lookup"><span data-stu-id="72f32-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72f32-146">Este exemplo não mostra como processar os exemplos de mídia provenientes do WMReader.</span><span class="sxs-lookup"><span data-stu-id="72f32-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="72f32-147">Para obter exemplos de como processar áudio/vídeo ou outros tipos de amostras de mídia, consulte outros exemplos, por exemplo, AudioPlayer, que estão incluídos no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="72f32-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-148">UncompAVIToWMV</span><span class="sxs-lookup"><span data-stu-id="72f32-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="72f32-149">Este exemplo de aplicativo de console mostra o código necessário para compactar um arquivo AVI para um arquivo WMV.</span><span class="sxs-lookup"><span data-stu-id="72f32-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="72f32-150">Ele mostra como mesclar exemplos de fluxos de áudio e vídeo de vários arquivos AVI e mesclá-los em fluxos semelhantes ou criar um novo fluxo com base no perfil de fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="72f32-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="72f32-151">Ele também mostra como criar um fluxo arbitrário, executar a codificação de passagem, adicionar o código de tempo SMPTE e aplicar a proteção DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="72f32-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-152">WMGenProfile/exe</span><span class="sxs-lookup"><span data-stu-id="72f32-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="72f32-153">Este exemplo foi atualizado a partir da versão 7,1.</span><span class="sxs-lookup"><span data-stu-id="72f32-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="72f32-154">Agora é um aplicativo de caixa de diálogo do MFC.</span><span class="sxs-lookup"><span data-stu-id="72f32-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="72f32-155">O exemplo de WMGenProfile demonstra o uso da biblioteca estática WMGenProfile.</span><span class="sxs-lookup"><span data-stu-id="72f32-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="72f32-156">Ele também serve como uma ferramenta para a criação de perfis.</span><span class="sxs-lookup"><span data-stu-id="72f32-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="72f32-157">Essa ferramenta destina-se a desenvolvedores familiarizados com o formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f32-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="72f32-158">A IU não foi testada quanto à experiência do usuário e não se destina a uma recomendação sobre como apresentar essas informações a um usuário.</span><span class="sxs-lookup"><span data-stu-id="72f32-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-159">WMGenProfile/lib</span><span class="sxs-lookup"><span data-stu-id="72f32-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="72f32-160">O exemplo da biblioteca GenProfile demonstra a criação de perfis.</span><span class="sxs-lookup"><span data-stu-id="72f32-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="72f32-161">Ele mostra como criar tipos de mídia e fluxos para vários tipos de fluxo (áudio, vídeo, script, imagem, transferência de arquivo e Web).</span><span class="sxs-lookup"><span data-stu-id="72f32-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="72f32-162">Ele não demonstra como trabalhar com perfis de sistema ou como converter perfis de sistema em perfis que especificam os codecs de áudio do Windows Media e vídeo 9 Series.</span><span class="sxs-lookup"><span data-stu-id="72f32-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-163">WMProp</span><span class="sxs-lookup"><span data-stu-id="72f32-163">WMProp</span></span></td>
<td><span data-ttu-id="72f32-164">Este aplicativo de console demonstra como recuperar atributos usando o objeto do editor de metadados e as informações de perfil do leitor.</span><span class="sxs-lookup"><span data-stu-id="72f32-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-165">WMStats</span><span class="sxs-lookup"><span data-stu-id="72f32-165">WMStats</span></span></td>
<td><span data-ttu-id="72f32-166">Esse aplicativo de console exibe as estatísticas de leitor e gravador.</span><span class="sxs-lookup"><span data-stu-id="72f32-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="72f32-167">Várias instâncias do WMStats também podem ser usadas simultaneamente em uma máquina.</span><span class="sxs-lookup"><span data-stu-id="72f32-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="72f32-168">Inicie uma instância como um servidor para enviar o fluxo para a rede e, em seguida, execute uma segunda instância como um cliente para verificar se o servidor está transmitindo corretamente.</span><span class="sxs-lookup"><span data-stu-id="72f32-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-169">WMSyncReader</span><span class="sxs-lookup"><span data-stu-id="72f32-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="72f32-170">Este exemplo de aplicativo de console mostra como ler um arquivo de mídia usando <strong>IWMSyncReader</strong> sem criar nenhum thread extra ou usar retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="72f32-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="72f32-171">Os seguintes recursos são implementados: lendo amostras compactadas ou descompactadas</span><span class="sxs-lookup"><span data-stu-id="72f32-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="72f32-172">Busca baseada em tempo</span><span class="sxs-lookup"><span data-stu-id="72f32-172">Time-based seeking</span></span><br/> <span data-ttu-id="72f32-173">Busca baseada em quadros</span><span class="sxs-lookup"><span data-stu-id="72f32-173">Frame-based seeking</span></span><br/> <span data-ttu-id="72f32-174">Fonte derivada de <strong>IStream</strong></span><span class="sxs-lookup"><span data-stu-id="72f32-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-175">WMVAppend</span><span class="sxs-lookup"><span data-stu-id="72f32-175">WMVAppend</span></span></td>
<td><span data-ttu-id="72f32-176">Esse aplicativo de console usa dois arquivos de mídia do Windows para entrada e tenta criar um arquivo de saída com o conteúdo do primeiro seguido pelo segundo.</span><span class="sxs-lookup"><span data-stu-id="72f32-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="72f32-177">O exemplo compara os perfis dos dois arquivos de entrada para garantir que eles sejam semelhantes o suficiente para serem acrescentados.</span><span class="sxs-lookup"><span data-stu-id="72f32-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="72f32-178">Se esse não for o caso, será exibida uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="72f32-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="72f32-179">Por exemplo, uma mensagem de erro ocorre quando um arquivo é somente áudio e o segundo é um arquivo de vídeo de áudio ou quando dois arquivos de áudio têm taxas de bits diferentes. O exemplo aceita fontes de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="72f32-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="72f32-180">No entanto, ao comparar os perfis das duas fontes de VBR, o exemplo ignora a diferença média da taxa de bits, pois dois fluxos de VBR terão taxas de bits médias diferentes, mesmo que tenham sido criados usando o mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="72f32-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="72f32-181">WMVAppend não pode comparar a taxa de bits de pico de fluxos de VBR de taxa de bits não restritos, ou o nível de qualidade de fluxos de VBR com base em qualidade, porque essas informações não existem nos arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="72f32-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="72f32-182">Portanto, é responsabilidade do usuário certificar-se de que dois arquivos de origem sejam criados usando o mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="72f32-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="72f32-183">Caso contrário, o conteúdo inválido poderá ser criado.</span><span class="sxs-lookup"><span data-stu-id="72f32-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-184">WMVCopy</span><span class="sxs-lookup"><span data-stu-id="72f32-184">WMVCopy</span></span></td>
<td><span data-ttu-id="72f32-185">Este exemplo mostra o código necessário para copiar um arquivo WMV.</span><span class="sxs-lookup"><span data-stu-id="72f32-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="72f32-186">Ele mostra como ler e gravar exemplos compactados, ler scripts e atributos de cabeçalho e modificar atributos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="72f32-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72f32-187">WMVNetWrite</span><span class="sxs-lookup"><span data-stu-id="72f32-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="72f32-188">Esse aplicativo de console mostra como um arquivo de mídia do Windows é transmitido pela Internet.</span><span class="sxs-lookup"><span data-stu-id="72f32-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="72f32-189">O exemplo requer que uma porta seja especificada e, em seguida, o arquivo pode ser reproduzido usando um player.</span><span class="sxs-lookup"><span data-stu-id="72f32-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72f32-190">WMVRecompress</span><span class="sxs-lookup"><span data-stu-id="72f32-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="72f32-191">Este aplicativo de console mostra como recompactar um arquivo WMV.</span><span class="sxs-lookup"><span data-stu-id="72f32-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="72f32-192">Ele demonstra a leitura de amostras não compactadas, a gravação de amostras descompactadas e a codificação de várias passagens, a saída de vários canais e a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="72f32-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="72f32-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72f32-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72f32-194">**Sobre o SDK do Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="72f32-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="72f32-195">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="72f32-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





