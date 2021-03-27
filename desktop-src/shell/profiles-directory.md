---
description: 'O sistema armazena informações de perfil de usuário em um diretório específico, que tem nomes diferentes em versões diferentes do Windows: &\# 0034; Documents and Settings&\# 0034; no Windows XP e &\# 0034; Os usuários&\# 0034; no Windows Vista e versões posteriores.'
title: Diretório de perfis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968000"
---
# <a name="profiles-directory"></a><span data-ttu-id="6966d-103">Diretório de perfis</span><span class="sxs-lookup"><span data-stu-id="6966d-103">Profiles Directory</span></span>

<span data-ttu-id="6966d-104">O sistema armazena informações de perfil de usuário em um diretório específico, que tem nomes diferentes em versões diferentes do Windows: "Documents and Settings" no Windows XP e "Users" no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6966d-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="6966d-105">Para obter o caminho do diretório de perfis, use a função [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="6966d-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="6966d-106">O diretório de perfis contém os seguintes subdiretórios para perfis de usuário.</span><span class="sxs-lookup"><span data-stu-id="6966d-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="6966d-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="6966d-107">Directory</span></span>                                      | <span data-ttu-id="6966d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6966d-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6966d-109">Usuários do ProgramData (Windows Vista ou posterior)/All</span><span class="sxs-lookup"><span data-stu-id="6966d-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="6966d-110">Informações do programa que se aplicam a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="6966d-110">Program information that applies to all users.</span></span> <span data-ttu-id="6966d-111">O diretório todos os usuários ainda existe no Windows Vista ou posterior, para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6966d-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="6966d-112">Padrão</span><span class="sxs-lookup"><span data-stu-id="6966d-112">Default</span></span>                                        | <span data-ttu-id="6966d-113">Informações de perfil que se aplicam ao usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="6966d-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="6966d-114">*Usuário*</span><span class="sxs-lookup"><span data-stu-id="6966d-114">*User*</span></span>                                         | <span data-ttu-id="6966d-115">Informações de perfil que se aplicam ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="6966d-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="6966d-116">Cada usuário tem seu próprio subdiretório de perfil.</span><span class="sxs-lookup"><span data-stu-id="6966d-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="6966d-117">Para obter o local do diretório ProgramData/todos os usuários, chame a função [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="6966d-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="6966d-118">O diretório raiz contém os seguintes subdiretórios:</span><span class="sxs-lookup"><span data-stu-id="6966d-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="6966d-119">Diretório</span><span class="sxs-lookup"><span data-stu-id="6966d-119">Directory</span></span>  | <span data-ttu-id="6966d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="6966d-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="6966d-121">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="6966d-121">Desktop</span></span>    | <span data-ttu-id="6966d-122">Atalhos a serem exibidos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6966d-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="6966d-123">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="6966d-123">Start Menu</span></span> | <span data-ttu-id="6966d-124">Itens de menu para o menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="6966d-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="6966d-125">Para obter o local do diretório do usuário padrão, chame a função [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="6966d-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="6966d-126">Para obter o local de um determinado diretório de usuário, chame a função [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="6966d-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="6966d-127">O usuário padrão e os diretórios de usuário específicos contêm os seguintes subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="6966d-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="6966d-128">Os diretórios em itálico indicam os diretórios que estão ocultos por padrão.</span><span class="sxs-lookup"><span data-stu-id="6966d-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="6966d-129">Você pode exibir esses diretórios selecionando a opção **Mostrar arquivos ocultos, pastas e unidades** no item do painel de controle de **Opções de pasta** .</span><span class="sxs-lookup"><span data-stu-id="6966d-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6966d-130">Diretório</span><span class="sxs-lookup"><span data-stu-id="6966d-130">Directory</span></span></th>
<th><span data-ttu-id="6966d-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="6966d-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6966d-132">Dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6966d-132">Application Data</span></span></td>
<td><span data-ttu-id="6966d-133">Dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6966d-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-134">Cookies</span><span class="sxs-lookup"><span data-stu-id="6966d-134">Cookies</span></span></td>
<td><span data-ttu-id="6966d-135">Cookies do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6966d-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6966d-136">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="6966d-136">Desktop</span></span></td>
<td><span data-ttu-id="6966d-137">Atalhos a serem exibidos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6966d-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-138">Favoritos</span><span class="sxs-lookup"><span data-stu-id="6966d-138">Favorites</span></span></td>
<td><span data-ttu-id="6966d-139">Links para sites favoritos.</span><span class="sxs-lookup"><span data-stu-id="6966d-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6966d-140">Configurações locais</span><span class="sxs-lookup"><span data-stu-id="6966d-140">Local Settings</span></span></td>
<td><span data-ttu-id="6966d-141">Configurações de aplicativo e dados que não são movidos com o perfil.</span><span class="sxs-lookup"><span data-stu-id="6966d-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="6966d-142">Normalmente, as configurações ou os dados nesse diretório são específicos do computador ou são muito grandes para serem movidos com eficiência.</span><span class="sxs-lookup"><span data-stu-id="6966d-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="6966d-143">Esse diretório contém as seguintes subpastas:</span><span class="sxs-lookup"><span data-stu-id="6966d-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="6966d-144">Dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6966d-144">Application Data</span></span></li>
<li><span data-ttu-id="6966d-145">Histórico</span><span class="sxs-lookup"><span data-stu-id="6966d-145">History</span></span></li>
<li><span data-ttu-id="6966d-146">Temp</span><span class="sxs-lookup"><span data-stu-id="6966d-146">Temp</span></span></li>
<li><span data-ttu-id="6966d-147">Arquivos Temporários da Internet</span><span class="sxs-lookup"><span data-stu-id="6966d-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-148">Meus Documentos</span><span class="sxs-lookup"><span data-stu-id="6966d-148">My Documents</span></span></td>
<td><span data-ttu-id="6966d-149">O local padrão para documentos que o usuário cria.</span><span class="sxs-lookup"><span data-stu-id="6966d-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="6966d-150">Por padrão, os aplicativos devem salvar arquivos de documento nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="6966d-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6966d-151"><em>NetHood</em></span><span class="sxs-lookup"><span data-stu-id="6966d-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="6966d-152">Atalhos para itens de ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="6966d-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-153"><em>PrintHood</em></span><span class="sxs-lookup"><span data-stu-id="6966d-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="6966d-154">Atalhos para itens de pasta da impressora.</span><span class="sxs-lookup"><span data-stu-id="6966d-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6966d-155"><em>Recente</em></span><span class="sxs-lookup"><span data-stu-id="6966d-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="6966d-156">Atalhos para os documentos usados mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="6966d-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="6966d-157">SendTo</span></span></td>
<td><span data-ttu-id="6966d-158">Atalhos para locais nos quais o usuário geralmente envia arquivos.</span><span class="sxs-lookup"><span data-stu-id="6966d-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6966d-159">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="6966d-159">Start Menu</span></span></td>
<td><span data-ttu-id="6966d-160">Itens de menu para o menu <strong>Iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="6966d-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6966d-161"><em>Modelos</em></span><span class="sxs-lookup"><span data-stu-id="6966d-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="6966d-162">Atalhos para itens de modelo.</span><span class="sxs-lookup"><span data-stu-id="6966d-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6966d-163">Para obter o local de subdiretórios desses diretórios, use as funções [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ou [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .</span><span class="sxs-lookup"><span data-stu-id="6966d-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



