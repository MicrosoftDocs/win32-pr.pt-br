---
title: Configurações do registro de monitoramento de pasta
description: Configurações do registro de monitoramento de pasta
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, configurações do registro de monitoramento de pasta
- Windows Media Player, configurações do registro de monitoramento de pasta de arquivos
- Windows Media Player, registro
- registro, configurações de monitoramento de pasta
- registro, configurações de monitoramento de pasta de arquivo
- registro, configurações do Windows Media Player
- configurações do registro de monitoramento de pasta
- configurações do registro de monitoramento da pasta de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366826"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="25560-111">Configurações do registro de monitoramento de pasta</span><span class="sxs-lookup"><span data-stu-id="25560-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="25560-112">O Windows Media Player 9 Series ou posterior pode monitorar pastas de arquivos para novos arquivos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="25560-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="25560-113">Quando o Player detecta um novo arquivo em uma pasta monitorada, ele adiciona automaticamente o arquivo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="25560-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="25560-114">Para o Windows Media Player 9 até o Windows Media Player 11, os usuários podem alterar a lista de pastas monitoradas clicando em **monitorar pastas** na guia Biblioteca da caixa de diálogo **Opções** .</span><span class="sxs-lookup"><span data-stu-id="25560-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="25560-115">Para o Windows Media Player 12, um usuário pode alterar a lista de pastas monitoradas seguindo as instruções no tópico [Adicionar itens à biblioteca do Windows Media Player](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span><span class="sxs-lookup"><span data-stu-id="25560-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="25560-116">Para o Windows Media Player 9 até o Windows Media Player 11, você pode adicionar programaticamente uma pasta a ser monitorada, adicionando um valor ao registro.</span><span class="sxs-lookup"><span data-stu-id="25560-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="25560-117">Para o Windows Media Player 12, você não pode usar o registro para adicionar ou remover programaticamente pastas a serem monitoradas.</span><span class="sxs-lookup"><span data-stu-id="25560-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="25560-118">Para o Windows Media Player 9 até o Windows Media Player 11, para adicionar uma pasta para monitoramento, você deve primeiro criar ou modificar dois valores na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="25560-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="25560-119">**HKEY \_ Current \_ user \\ software \\ usuário \\ preferências do Microsoft MediaPlayer \\\\**</span><span class="sxs-lookup"><span data-stu-id="25560-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="25560-120">Os novos valores devem ser nomeados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="25560-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="25560-121">Nome</span><span class="sxs-lookup"><span data-stu-id="25560-121">Name</span></span>                           | <span data-ttu-id="25560-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="25560-122">Type</span></span>           | <span data-ttu-id="25560-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="25560-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25560-124">**TrackFoldersDirectories**</span><span class="sxs-lookup"><span data-stu-id="25560-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="25560-125">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="25560-125">**REG\_DWORD**</span></span> | <span data-ttu-id="25560-126">Um valor **DWORD** que representa a contagem de pastas a serem monitoradas.</span><span class="sxs-lookup"><span data-stu-id="25560-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="25560-127">Isso deve corresponder à contagem de \**TrackFoldersDirectories \* \* \* X* valores.</span><span class="sxs-lookup"><span data-stu-id="25560-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="25560-128">\**TrackFoldersDirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="25560-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="25560-129">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="25560-129">**REG\_SZ**</span></span>    | <span data-ttu-id="25560-130">Um valor de cadeia de caracteres que representa o caminho da pasta a ser monitorada.</span><span class="sxs-lookup"><span data-stu-id="25560-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="25560-131">Cada pasta a ser monitorada requer um valor separado.</span><span class="sxs-lookup"><span data-stu-id="25560-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="25560-132">O sufixo *X* é um inteiro que sempre deve começar em 0 e, em seguida, incrementado em 1.</span><span class="sxs-lookup"><span data-stu-id="25560-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="25560-133">O Windows Media Player também monitora as subpastas da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="25560-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="25560-134">Por exemplo, para adicionar a primeira pasta a ser monitorada, adicione o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="25560-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="25560-135">Em seguida, crie o valor da contagem:</span><span class="sxs-lookup"><span data-stu-id="25560-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="25560-136">Para adicionar uma segunda pasta a ser monitorada, adicione o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="25560-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="25560-137">Em seguida, aumente o valor da contagem:</span><span class="sxs-lookup"><span data-stu-id="25560-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="25560-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25560-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25560-139">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="25560-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




