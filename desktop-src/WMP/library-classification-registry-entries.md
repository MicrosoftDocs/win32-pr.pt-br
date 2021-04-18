---
title: Entradas do registro de classificação de biblioteca
description: Entradas do registro de classificação de biblioteca
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, biblioteca
- Windows Media Player, entradas do registro de classificação
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas de classificação de biblioteca
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- biblioteca, entradas do registro de classificação
- biblioteca, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781425"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="dc397-113">Entradas do registro de classificação de biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc397-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="dc397-114">Quando o Windows Media Player encontra um arquivo de mídia que tem uma extensão de nome de arquivo Personalizada, ele não sabe se o arquivo deve ser classificado como áudio, vídeo ou algum outro tipo.</span><span class="sxs-lookup"><span data-stu-id="dc397-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="dc397-115">Por padrão, o Windows Media Player coloca esses arquivos na parte de outra mídia da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dc397-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="dc397-116">Se os arquivos de mídia digital tiverem um formato personalizado, você poderá fornecer ao Windows Media Player informações sobre onde os arquivos devem aparecer na biblioteca do Player, colocando duas entradas no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc397-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="dc397-117">Uma entrada é exibida na subchave a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc397-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="dc397-118">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensões**</span><span class="sxs-lookup"><span data-stu-id="dc397-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="dc397-119">A entrada do registro tem o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc397-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="dc397-120">Nome</span><span class="sxs-lookup"><span data-stu-id="dc397-120">Name</span></span>                                                  | <span data-ttu-id="dc397-121">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dc397-121">Data type</span></span>   | <span data-ttu-id="dc397-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dc397-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="dc397-123">A extensão de nome de arquivo sem o separador de ponto (.)</span><span class="sxs-lookup"><span data-stu-id="dc397-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="dc397-124">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="dc397-124">**REG\_SZ**</span></span> | <span data-ttu-id="dc397-125">Uma cadeia de caracteres que especifica um local de biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc397-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="dc397-126">A outra entrada do registro é exibida na subchave a seguir que você cria.</span><span class="sxs-lookup"><span data-stu-id="dc397-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="dc397-127">**HKEY \_ CustomExtension de classes \_ raiz \\** </span><span class="sxs-lookup"><span data-stu-id="dc397-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="dc397-128">em que *customExtension* é a extensão de nome de arquivo, incluindo o separador de ponto (.).</span><span class="sxs-lookup"><span data-stu-id="dc397-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="dc397-129">A entrada do registro tem o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc397-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="dc397-130">Nome</span><span class="sxs-lookup"><span data-stu-id="dc397-130">Name</span></span>          | <span data-ttu-id="dc397-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dc397-131">Data type</span></span>   | <span data-ttu-id="dc397-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dc397-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="dc397-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="dc397-133">PerceivedType</span></span> | <span data-ttu-id="dc397-134">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="dc397-134">**REG\_SZ**</span></span> | <span data-ttu-id="dc397-135">Uma cadeia de caracteres que especifica um local de biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc397-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="dc397-136">Ambas as entradas do registro devem ter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="dc397-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="dc397-137">Os valores possíveis são fornecidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc397-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="dc397-138">Valor</span><span class="sxs-lookup"><span data-stu-id="dc397-138">Value</span></span> | <span data-ttu-id="dc397-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc397-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc397-140">áudio</span><span class="sxs-lookup"><span data-stu-id="dc397-140">audio</span></span> | <span data-ttu-id="dc397-141">Os arquivos que têm a extensão personalizada aparecem na parte de música da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dc397-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="dc397-142">video</span><span class="sxs-lookup"><span data-stu-id="dc397-142">video</span></span> | <span data-ttu-id="dc397-143">Os arquivos que têm a extensão personalizada aparecem na parte de vídeo da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dc397-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="dc397-144">Por exemplo, as seguintes entradas de registro especificam que os arquivos que têm a extensão de nome de arquivo. xyz aparecerão na parte de música da biblioteca:</span><span class="sxs-lookup"><span data-stu-id="dc397-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="dc397-145">Observe que qualquer código que tente gravar no registro no computador do usuário poderá gravar na \_ subárvore do computador local hKey \_ somente se o usuário atual tiver privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="dc397-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="dc397-146">As entradas do registro de classificação de biblioteca têm suporte nas seguintes versões do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dc397-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="dc397-147">Windows Media Player 9 Series com hotfix 823275</span><span class="sxs-lookup"><span data-stu-id="dc397-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="dc397-148">Windows Media Player 10 e posterior</span><span class="sxs-lookup"><span data-stu-id="dc397-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc397-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc397-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc397-150">**Configurações do registro de extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="dc397-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




