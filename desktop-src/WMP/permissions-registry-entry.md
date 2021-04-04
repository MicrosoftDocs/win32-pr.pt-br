---
title: Entrada de registro de permissões
description: Entrada de registro de permissões
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, permissões
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, permissões
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- permissões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007088"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="4a1f8-111">Entrada de registro de permissões</span><span class="sxs-lookup"><span data-stu-id="4a1f8-111">Permissions Registry Entry</span></span>

<span data-ttu-id="4a1f8-112">Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="4a1f8-113">A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4a1f8-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="4a1f8-114">Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **permissões** .</span><span class="sxs-lookup"><span data-stu-id="4a1f8-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="4a1f8-115">A entrada de **permissões** especifica as ações que o Windows Media Player tem permissão para executar em arquivos que têm a extensão personalizada.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="4a1f8-116">A entrada de **permissões** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="4a1f8-117">Nome</span><span class="sxs-lookup"><span data-stu-id="4a1f8-117">Name</span></span>        | <span data-ttu-id="4a1f8-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a1f8-118">Type</span></span>           | <span data-ttu-id="4a1f8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4a1f8-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="4a1f8-120">Permissões</span><span class="sxs-lookup"><span data-stu-id="4a1f8-120">Permissions</span></span> | <span data-ttu-id="4a1f8-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a1f8-121">**REG\_DWORD**</span></span> | <span data-ttu-id="4a1f8-122">Um conjunto de sinalizadores, cada um concedendo permissão para uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="4a1f8-123">O valor da entrada **Permissions** é uma operação OR de um ou **mais dos sinalizadores** a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="4a1f8-124">Sinalizador (valor decimal)</span><span class="sxs-lookup"><span data-stu-id="4a1f8-124">Flag (decimal value)</span></span> | <span data-ttu-id="4a1f8-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a1f8-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1f8-126">1</span><span class="sxs-lookup"><span data-stu-id="4a1f8-126">1</span></span>                    | <span data-ttu-id="4a1f8-127">Permissão para reprodução.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-127">Permission for playback.</span></span> <span data-ttu-id="4a1f8-128">Arquivos com a extensão de nome de arquivo registrado podem ser reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="4a1f8-129">2</span><span class="sxs-lookup"><span data-stu-id="4a1f8-129">2</span></span>                    | <span data-ttu-id="4a1f8-130">Permissão para drop de pasta.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-130">Permission for folder drop.</span></span> <span data-ttu-id="4a1f8-131">Os arquivos com a extensão de nome de arquivo registrado serão incluídos na playlist criada quando o usuário arrastar uma pasta que contém os arquivos e o descartará na interface do usuário do Player.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="4a1f8-132">4</span><span class="sxs-lookup"><span data-stu-id="4a1f8-132">4</span></span>                    | <span data-ttu-id="4a1f8-133">Permissão para CD de mídia.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-133">Permission for media CD.</span></span> <span data-ttu-id="4a1f8-134">Os arquivos com a extensão de nome de arquivo registrado serão incluídos na playlist criada quando um CD que contém os arquivos for inserido na unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="4a1f8-135">8</span><span class="sxs-lookup"><span data-stu-id="4a1f8-135">8</span></span>                    | <span data-ttu-id="4a1f8-136">Permissão para a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-136">Permission for the library.</span></span> <span data-ttu-id="4a1f8-137">Arquivos com a extensão de nome de arquivo registrado podem ser adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="4a1f8-138">Necessário para plug-ins de conversão.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="4a1f8-139">16</span><span class="sxs-lookup"><span data-stu-id="4a1f8-139">16</span></span>                   | <span data-ttu-id="4a1f8-140">Permissão para streaming HTML.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-140">Permission for HTML streaming.</span></span> <span data-ttu-id="4a1f8-141">Os arquivos com a extensão de nome de arquivo registrado serão inseridos no cache do Internet Explorer quando entregues de um fluxo da Web.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="4a1f8-142">128</span><span class="sxs-lookup"><span data-stu-id="4a1f8-142">128</span></span>                  | <span data-ttu-id="4a1f8-143">Permissão para transcodificação.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-143">Permission for transcoding.</span></span> <span data-ttu-id="4a1f8-144">Arquivos com a extensão de nome de arquivo registrado podem ser transcodificados para o formato de mídia do Windows em determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="4a1f8-145">Consulte [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="4a1f8-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="4a1f8-146">Requer o Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="4a1f8-147">Quando o usuário tenta reproduzir um arquivo de mídia que tem uma extensão de nome de arquivo Personalizada, o Windows Media Player procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="4a1f8-148">Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="4a1f8-149">Se você criar arquivos de mídia digital com extensões de nome de arquivo personalizadas, poderá evitar que esse aviso apareça no computador do usuário registrando a extensão de nome de arquivo e fornecendo uma entrada de **permissões** .</span><span class="sxs-lookup"><span data-stu-id="4a1f8-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="4a1f8-150">A entrada de **permissões** (exceto para o valor de sinalizador 128) é suportada pelo Windows Media Player 9 Series e posterior.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="4a1f8-151">O valor do sinalizador 128 é suportado pelo Windows Media Player 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4a1f8-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a1f8-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a1f8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a1f8-153">**Configurações do registro de extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="4a1f8-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




