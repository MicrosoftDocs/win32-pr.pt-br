---
description: ICE64 verifica se os novos diretórios no perfil do usuário são removidos corretamente em cenários de roaming.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506038"
---
# <a name="ice64"></a><span data-ttu-id="27c7b-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="27c7b-103">ICE64</span></span>

<span data-ttu-id="27c7b-104">ICE64 verifica se os novos diretórios no perfil do usuário são removidos corretamente em cenários de roaming.</span><span class="sxs-lookup"><span data-stu-id="27c7b-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="27c7b-105">A falha em corrigir um aviso ou erro relatado por ICE64 geralmente leva a problemas na limpeza completa do computador durante uma desinstalação.</span><span class="sxs-lookup"><span data-stu-id="27c7b-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="27c7b-106">Quando um usuário móvel que instalou o aplicativo faz logon em um computador pela primeira vez, todo o perfil é copiado para baixo no computador.</span><span class="sxs-lookup"><span data-stu-id="27c7b-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="27c7b-107">No anúncio (que ocorre após o download do perfil móvel), o instalador verifica se o diretório já existe e, portanto, não o exclui na desinstalação.</span><span class="sxs-lookup"><span data-stu-id="27c7b-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="27c7b-108">Isso deixa o diretório no computador do usuário permanentemente.</span><span class="sxs-lookup"><span data-stu-id="27c7b-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="27c7b-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="27c7b-109">Result</span></span>

<span data-ttu-id="27c7b-110">O ICE64 posta um aviso ou um erro em uma situação de roaming se um novo diretório no perfil do usuário que deve ser removido não for removido.</span><span class="sxs-lookup"><span data-stu-id="27c7b-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="27c7b-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="27c7b-111">Example</span></span>

<span data-ttu-id="27c7b-112">ICE64 relata o seguinte erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="27c7b-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="27c7b-113">A pasta ' MyOtherFolder ' é uma pasta de perfil Personalizada.</span><span class="sxs-lookup"><span data-stu-id="27c7b-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="27c7b-114">Como não está listado na tabela removerfile, ele não é removido em alguns cenários.</span><span class="sxs-lookup"><span data-stu-id="27c7b-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="27c7b-115">Para corrigir esse erro, crie uma linha para a pasta na tabela RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="27c7b-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="27c7b-116">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="27c7b-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="27c7b-117">Diretório</span><span class="sxs-lookup"><span data-stu-id="27c7b-117">Directory</span></span>     | <span data-ttu-id="27c7b-118">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="27c7b-118">Directory\_Parent</span></span> | <span data-ttu-id="27c7b-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="27c7b-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="27c7b-120">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-120">AppDataFolder</span></span> | <span data-ttu-id="27c7b-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="27c7b-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="27c7b-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-122">MyFolder</span></span>      | <span data-ttu-id="27c7b-123">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-123">AppDataFolder</span></span>     | <span data-ttu-id="27c7b-124">DataFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-124">DataFolder</span></span>  |
| <span data-ttu-id="27c7b-125">MyOtherFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-125">MyOtherFolder</span></span> | <span data-ttu-id="27c7b-126">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-126">AppDataFolder</span></span>     | <span data-ttu-id="27c7b-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="27c7b-127">DataFolder2</span></span> |



 

[<span data-ttu-id="27c7b-128">Remover Tabelafile</span><span class="sxs-lookup"><span data-stu-id="27c7b-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="27c7b-129">FileKey</span><span class="sxs-lookup"><span data-stu-id="27c7b-129">FileKey</span></span> | <span data-ttu-id="27c7b-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="27c7b-130">Component\_</span></span> | <span data-ttu-id="27c7b-131">FileName</span><span class="sxs-lookup"><span data-stu-id="27c7b-131">FileName</span></span> | <span data-ttu-id="27c7b-132">DirProperty</span><span class="sxs-lookup"><span data-stu-id="27c7b-132">DirProperty</span></span> | <span data-ttu-id="27c7b-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="27c7b-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="27c7b-134">Key1</span><span class="sxs-lookup"><span data-stu-id="27c7b-134">Key1</span></span>    | <span data-ttu-id="27c7b-135">Component1</span><span class="sxs-lookup"><span data-stu-id="27c7b-135">Component1</span></span>  |          | <span data-ttu-id="27c7b-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="27c7b-136">MyFolder</span></span>    | <span data-ttu-id="27c7b-137">2</span><span class="sxs-lookup"><span data-stu-id="27c7b-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="27c7b-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27c7b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c7b-139">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="27c7b-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



