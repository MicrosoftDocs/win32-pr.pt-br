---
title: Subchave ConvertPluginCLSID
description: Subchave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player, subchave ConvertPluginCLSID
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, subchave ConvertPluginCLSID
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Subchave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005611"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="c8fb3-111">Subchave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="c8fb3-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="c8fb3-112">Quando o Windows Media Player 11 encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="c8fb3-113">A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c8fb3-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="c8fb3-114">Em alguns casos, a subchave da extensão tem uma subchave chamada **ConvertPluginCLSID**.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="c8fb3-115">Por exemplo, suponha que você tenha criado um formato de arquivo personalizado (com a extensão de nome de arquivo. xyz) e um plug-in de conversão que converta os arquivos em um formato suportado pelo Windows Media Player. em seguida, você armazenaria a ID de classe do plug-in em uma ou ambas as subchaves a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="c8fb3-116">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Extensions \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="c8fb3-117">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="c8fb3-118">A subchave **ConvertPluginCLSID** especifica as IDs de classe de plug-ins que o Windows Media Player pode usar para converter um arquivo de mídia de seu formato personalizado em um formato suportado pelo Player.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="c8fb3-119">A subchave **ConvertPluginCLSID** tem as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="c8fb3-120">Uma entrada padrão que representa o plug-in de conversão padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="c8fb3-121">Uma entrada nomeada que representa o plug-in de conversão padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="c8fb3-122">Entradas nomeadas adicionais que representam plug-ins alternativos de conversão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="c8fb3-123">Por exemplo, suponha que um formato de arquivo personalizado tenha um plug-in de conversão padrão e dois plug-ins alternativos de conversão. As entradas do registro na subchave **ConvertPluginCLSID** teriam o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="c8fb3-124">Nome</span><span class="sxs-lookup"><span data-stu-id="c8fb3-124">Name</span></span>                                                                          | <span data-ttu-id="c8fb3-125">Type</span><span class="sxs-lookup"><span data-stu-id="c8fb3-125">Type</span></span>        | <span data-ttu-id="c8fb3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c8fb3-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="c8fb3-127">Padrão</span><span class="sxs-lookup"><span data-stu-id="c8fb3-127">Default</span></span>                                                                       | <span data-ttu-id="c8fb3-128">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-128">**REG\_SZ**</span></span> | <span data-ttu-id="c8fb3-129">A ID da classe, no formato do registro, do plug-in de conversão padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="c8fb3-130">A ID da classe, no formato do registro, do plug-in de conversão padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="c8fb3-131">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-131">**REG\_SZ**</span></span> | <span data-ttu-id="c8fb3-132">O nome amigável do plug-in de conversão padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="c8fb3-133">A ID da classe, no formato do registro, do primeiro plug-in de conversão alternativo.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="c8fb3-134">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-134">**REG\_SZ**</span></span> | <span data-ttu-id="c8fb3-135">O nome amigável do primeiro plug-in de conversão alternativo.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="c8fb3-136">A ID da classe, no formato do registro, do segundo plug-in de conversão alternativo.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="c8fb3-137">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-137">**REG\_SZ**</span></span> | <span data-ttu-id="c8fb3-138">O nome amigável do segundo plug-in de conversão alternativo.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="c8fb3-139">Observe que o plug-in de conversão padrão é representado por duas entradas do registro: a entrada padrão e uma entrada nomeada.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="c8fb3-140">O Windows Media Player usa a entrada padrão para determinar qual plug-in é o plug-in de conversão padrão (primário).</span><span class="sxs-lookup"><span data-stu-id="c8fb3-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="c8fb3-141">O Windows Media Player usa as entradas nomeadas para obter nomes amigáveis para todos os plug-ins de conversão, incluindo o plug-in padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="c8fb3-142">O nome amigável de um plug-in de conversão é determinado pela empresa que cria o plug-in.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="c8fb3-143">O Windows Media Player pode exibir o nome amigável em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="c8fb3-144">Quando o Windows Media Player tenta converter um arquivo de um formato personalizado em um formato padrão, ele primeiro carrega o plug-in padrão.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="c8fb3-145">Se o plug-in padrão não converter o arquivo e retornar o proprietário do arquivo desconhecido do plug-in de conversão do NS \_ e \_ WMP \_ \_ \_ \_ \_ , o Player carregará cada plug-in alternativo até que ocorra uma conversão bem-sucedida ou que não haja mais plug-ins para tentar.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="c8fb3-146">O Player não exibirá uma mensagem de aviso se nenhum plug-in de conversão for encontrado para a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="c8fb3-147">A entrada do registro **ConvertPluginCLSID** tem suporte do Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c8fb3-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8fb3-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8fb3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8fb3-149">**Configurações do registro de extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="c8fb3-150">**Plug-ins de conversão do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c8fb3-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




