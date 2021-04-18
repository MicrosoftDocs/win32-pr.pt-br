---
description: O ICE91 lançará um aviso se um arquivo, arquivo. ini ou arquivo de atalho for instalado em um diretório somente por usuário.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752649"
---
# <a name="ice91"></a><span data-ttu-id="61a73-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="61a73-103">ICE91</span></span>

<span data-ttu-id="61a73-104">O ICE91 lançará um aviso se um arquivo, arquivo. ini ou arquivo de atalho for instalado em um diretório somente por usuário.</span><span class="sxs-lookup"><span data-stu-id="61a73-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="61a73-105">Esses avisos serão inofensivos se o pacote for usado apenas para instalação no contexto de [instalação](installation-context.md) por usuário e nunca for usado para instalações por máquina.</span><span class="sxs-lookup"><span data-stu-id="61a73-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="61a73-106">Arquivos, arquivos. ini ou atalhos em diretórios somente por usuário são instalados em um perfil de usuário específico.</span><span class="sxs-lookup"><span data-stu-id="61a73-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="61a73-107">Mesmo que o usuário defina a propriedade [**AllUsers**](allusers.md) para instalações por computador, arquivos, arquivos. ini ou atalhos em diretórios somente por usuário não serão copiados no perfil "todos os usuários" e não estarão disponíveis para outros usuários.</span><span class="sxs-lookup"><span data-stu-id="61a73-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="61a73-108">Os diretórios somente por usuário não variam com a propriedade **AllUsers** .</span><span class="sxs-lookup"><span data-stu-id="61a73-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="61a73-109">A seguir está uma lista dos diretórios somente por usuário:</span><span class="sxs-lookup"><span data-stu-id="61a73-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="61a73-110">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-110">AppDataFolder</span></span>
-   <span data-ttu-id="61a73-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-111">FavoritesFolder</span></span>
-   <span data-ttu-id="61a73-112">NetHoodFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-112">NetHoodFolder</span></span>
-   <span data-ttu-id="61a73-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-113">PersonalFolder</span></span>
-   <span data-ttu-id="61a73-114">PrintHoodFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="61a73-115">RecentFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-115">RecentFolder</span></span>
-   <span data-ttu-id="61a73-116">SendToFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-116">SendToFolder</span></span>
-   <span data-ttu-id="61a73-117">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="61a73-118">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="61a73-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="61a73-119">Result</span></span>

<span data-ttu-id="61a73-120">ICE91 posta os seguintes avisos.</span><span class="sxs-lookup"><span data-stu-id="61a73-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="61a73-121">Aviso de ICE91</span><span class="sxs-lookup"><span data-stu-id="61a73-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="61a73-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="61a73-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a73-123">O arquivo ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="61a73-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="61a73-124">Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada.</span><span class="sxs-lookup"><span data-stu-id="61a73-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="61a73-125">O arquivo é instalado em um diretório somente por usuário.</span><span class="sxs-lookup"><span data-stu-id="61a73-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="61a73-126">Ele não é instalado em cada perfil de usuário durante uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="61a73-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="61a73-127">O IniFile ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="61a73-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="61a73-128">Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada.</span><span class="sxs-lookup"><span data-stu-id="61a73-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="61a73-129">O arquivo. ini é instalado em um diretório somente por usuário.</span><span class="sxs-lookup"><span data-stu-id="61a73-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="61a73-130">Ele não é instalado em cada perfil de usuário durante uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="61a73-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="61a73-131">O atalho ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="61a73-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="61a73-132">Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada.</span><span class="sxs-lookup"><span data-stu-id="61a73-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="61a73-133">O atalho é instalado em um diretório somente por usuário.</span><span class="sxs-lookup"><span data-stu-id="61a73-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="61a73-134">Ele não é instalado em cada perfil de usuário durante uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="61a73-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="61a73-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="61a73-135">Example</span></span>

<span data-ttu-id="61a73-136">ICE91 relata os seguintes avisos para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="61a73-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="61a73-137">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="61a73-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="61a73-138">Arquivo</span><span class="sxs-lookup"><span data-stu-id="61a73-138">File</span></span>  | <span data-ttu-id="61a73-139">Componente\_</span><span class="sxs-lookup"><span data-stu-id="61a73-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="61a73-140">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="61a73-140">File1</span></span> | <span data-ttu-id="61a73-141">C1</span><span class="sxs-lookup"><span data-stu-id="61a73-141">C1</span></span>          |



 

<span data-ttu-id="61a73-142">[Tabela de componentes](component-table.md) (parcial) (parcial) (parcial) (parcial)</span><span class="sxs-lookup"><span data-stu-id="61a73-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="61a73-143">Componente</span><span class="sxs-lookup"><span data-stu-id="61a73-143">Component</span></span> | <span data-ttu-id="61a73-144">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="61a73-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="61a73-145">C1</span><span class="sxs-lookup"><span data-stu-id="61a73-145">C1</span></span>        | <span data-ttu-id="61a73-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="61a73-146">MyDir</span></span>       |



 

[<span data-ttu-id="61a73-147">Tabela IniFile</span><span class="sxs-lookup"><span data-stu-id="61a73-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="61a73-148">IniFile</span><span class="sxs-lookup"><span data-stu-id="61a73-148">IniFile</span></span>  | <span data-ttu-id="61a73-149">DirProperty</span><span class="sxs-lookup"><span data-stu-id="61a73-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="61a73-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="61a73-150">IniFile1</span></span> | <span data-ttu-id="61a73-151">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="61a73-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="61a73-152">Tabela de atalho</span><span class="sxs-lookup"><span data-stu-id="61a73-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="61a73-153">Atalho</span><span class="sxs-lookup"><span data-stu-id="61a73-153">Shortcut</span></span>  | <span data-ttu-id="61a73-154">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="61a73-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="61a73-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="61a73-155">Shortcut1</span></span> | <span data-ttu-id="61a73-156">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="61a73-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="61a73-157">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="61a73-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="61a73-158">Diretório</span><span class="sxs-lookup"><span data-stu-id="61a73-158">Directory</span></span>     | <span data-ttu-id="61a73-159">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="61a73-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="61a73-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="61a73-160">MyDir</span></span>         | <span data-ttu-id="61a73-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="61a73-162">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="61a73-162">MyIniDir</span></span>      | <span data-ttu-id="61a73-163">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="61a73-164">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="61a73-164">MyShortcutDir</span></span> | <span data-ttu-id="61a73-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="61a73-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="61a73-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61a73-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a73-167">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="61a73-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



