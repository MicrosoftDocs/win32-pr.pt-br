---
title: Configurações do registro de extensão de nome de arquivo
description: Configurações do registro de extensão de nome de arquivo
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, registro
- Windows Media Player, extensões de nome de arquivo
- registro, extensões de nome de arquivo
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636719"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="08b19-108">Configurações do registro de extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="08b19-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="08b19-109">Se os arquivos de mídia digital tiverem um formato personalizado, você poderá fornecer ao Windows Media Player informações sobre seu formato personalizado colocando entradas no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="08b19-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="08b19-110">O Windows Media Player inspeciona as entradas do registro para determinar como ele deve lidar com seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="08b19-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="08b19-111">A lista a seguir mostra várias coisas que você pode fazer criando entradas do registro que pertencem ao seu formato de arquivo de mídia personalizado.</span><span class="sxs-lookup"><span data-stu-id="08b19-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="08b19-112">Conceda permissão para que o Player reproduza, copie ou transcodifique seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="08b19-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="08b19-113">Especifique a tecnologia subjacente que o Player deve usar para reproduzir os arquivos.</span><span class="sxs-lookup"><span data-stu-id="08b19-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="08b19-114">Especifique onde o Player deve exibir os arquivos em seu modo de exibição de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="08b19-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="08b19-115">Especifique um plug-in que o Player deve usar para converter os arquivos em um formato padrão.</span><span class="sxs-lookup"><span data-stu-id="08b19-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="08b19-116">Especifique um código de formato de MTP (protocolo de transporte de mídia) que o Player possa usar para determinar se um dispositivo portátil específico dá suporte ao seu formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="08b19-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="08b19-117">A maioria das entradas que você fornece estará sob uma subchave associada à extensão de nome de arquivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="08b19-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="08b19-118">Você pode criar essa subchave na \_ \_ subárvore do computador local hKey e na \_ subárvore do usuário atual do hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="08b19-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="08b19-119">O Windows Media Player primeiro procura na \_ \_ subárvore do computador local HKEY.</span><span class="sxs-lookup"><span data-stu-id="08b19-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="08b19-120">Se ele não encontrar o que precisa lá, ele procurará na \_ subárvore atual do usuário do hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="08b19-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="08b19-121">Observe que qualquer código que tente gravar no registro no computador do usuário poderá gravar na \_ subárvore do computador local hKey \_ somente se o usuário atual tiver privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="08b19-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="08b19-122">Para gravar informações sobre o formato de arquivo personalizado na \_ \_ subárvore do computador local hKey, crie a subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="08b19-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="08b19-123">**HKEY \_ \_Software da máquina local \\ \\ \\ \\ \\ extensões \\ de wmplayer multimídia da Microsoft** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="08b19-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="08b19-124">em que *customExtension* é a extensão de nome de arquivo, incluindo o separador de ponto (.).</span><span class="sxs-lookup"><span data-stu-id="08b19-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="08b19-125">Por exemplo, se a extensão para seu formato de arquivo personalizado for. xyz, crie a subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="08b19-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="08b19-126">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Extensions \\ . xyz**</span><span class="sxs-lookup"><span data-stu-id="08b19-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="08b19-127">Para gravar informações sobre o formato de arquivo personalizado na \_ subárvore do usuário atual do hKey \_ , crie a subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="08b19-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="08b19-128">**HKEY \_ \_ \\ Software do usuário \\ atual \\ \\ \\ extensões \\ do Microsoft MediaPlayer Player** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="08b19-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="08b19-129">Você pode escrever uma ou mais das seguintes entradas em sua subchave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="08b19-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="08b19-130">**Permissões**</span><span class="sxs-lookup"><span data-stu-id="08b19-130">**Permissions**</span></span>
-   <span data-ttu-id="08b19-131">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="08b19-131">**Runtime**</span></span>
-   <span data-ttu-id="08b19-132">**FormatCode**</span><span class="sxs-lookup"><span data-stu-id="08b19-132">**FormatCode**</span></span>

<span data-ttu-id="08b19-133">Para especificar plug-ins de conversão para seu formato de arquivo de mídia personalizado, crie uma subchave **ConvertPluginCLSID** em sua subchave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="08b19-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="08b19-134">Para especificar onde o Windows Media Player deve exibir os arquivos em seu modo de exibição de biblioteca, escreva uma entrada que represente o formato de arquivo personalizado na subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="08b19-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="08b19-135">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensões**</span><span class="sxs-lookup"><span data-stu-id="08b19-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="08b19-136">Os tópicos a seguir descrevem as subchaves e entradas do registro que fornecem ao Windows Media Player informações sobre formatos de arquivo de mídia personalizados.</span><span class="sxs-lookup"><span data-stu-id="08b19-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="08b19-137">Entrada de registro de permissões</span><span class="sxs-lookup"><span data-stu-id="08b19-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="08b19-138">Entrada de registro de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="08b19-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="08b19-139">Entrada do registro FormatCode</span><span class="sxs-lookup"><span data-stu-id="08b19-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="08b19-140">Entradas do registro de classificação de biblioteca</span><span class="sxs-lookup"><span data-stu-id="08b19-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="08b19-141">Subchave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="08b19-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="08b19-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08b19-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08b19-143">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="08b19-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="08b19-144">**Plug-ins de conversão do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="08b19-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




