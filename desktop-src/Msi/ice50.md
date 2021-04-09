---
description: ICE50 verifica se os ícones de atalho estão especificados para exibição correta e correspondem à extensão do arquivo de destino.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922329"
---
# <a name="ice50"></a><span data-ttu-id="6c934-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="6c934-103">ICE50</span></span>

<span data-ttu-id="6c934-104">ICE50 verifica se os ícones de atalho estão especificados para exibição correta e correspondem à extensão do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6c934-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="6c934-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="6c934-105">Result</span></span>

<span data-ttu-id="6c934-106">ICE50 posta uma mensagem de erro se a extensão do ícone e dos arquivos de destino não coincidem.</span><span class="sxs-lookup"><span data-stu-id="6c934-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="6c934-107">ICE50 posta um aviso se os ícones são armazenados em arquivos que não têm uma extensão. exe ou. ico.</span><span class="sxs-lookup"><span data-stu-id="6c934-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="6c934-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6c934-108">Example</span></span>

<span data-ttu-id="6c934-109">ICE50 relata o seguinte erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="6c934-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="6c934-110">Erro ou aviso do ICE50</span><span class="sxs-lookup"><span data-stu-id="6c934-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="6c934-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c934-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c934-112">A extensão do ícone ' Icon2. dat ' para o atalho ' Shortcut2 ' não corresponde à extensão do arquivo de chave para o componente ' Component2 '.</span><span class="sxs-lookup"><span data-stu-id="6c934-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="6c934-113">Se as extensões do ícone e o arquivo de destino não corresponderem, o atalho não terá o menu de contexto correto quando o componente for anunciado.</span><span class="sxs-lookup"><span data-stu-id="6c934-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="6c934-114">Para corrigir esse erro, renomeie o ícone para corresponder à extensão do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6c934-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="6c934-115">A extensão do ícone ' Icon1.bat ' para o atalho ' Shortcut1 ' não é "exe" ou "ico".</span><span class="sxs-lookup"><span data-stu-id="6c934-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="6c934-116">O ícone não será exibido corretamente.</span><span class="sxs-lookup"><span data-stu-id="6c934-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="6c934-117">Nem todas as versões do Shell exibem corretamente os ícones armazenados em arquivos que não têm extensões de "exe" ou "ico".</span><span class="sxs-lookup"><span data-stu-id="6c934-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="6c934-118">Para corrigir esse aviso, renomeie o ícone tem uma extensão de "exe" ou "ico".</span><span class="sxs-lookup"><span data-stu-id="6c934-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="6c934-119">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6c934-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="6c934-120">Arquivo</span><span class="sxs-lookup"><span data-stu-id="6c934-120">File</span></span>  | <span data-ttu-id="6c934-121">FileName</span><span class="sxs-lookup"><span data-stu-id="6c934-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="6c934-122">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="6c934-122">File1</span></span> | <span data-ttu-id="6c934-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="6c934-123">File1.bat</span></span> |
| <span data-ttu-id="6c934-124">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="6c934-124">File2</span></span> | <span data-ttu-id="6c934-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="6c934-125">File2.pl</span></span>  |



 

<span data-ttu-id="6c934-126">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6c934-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="6c934-127">Recurso</span><span class="sxs-lookup"><span data-stu-id="6c934-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="6c934-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="6c934-128">Feature1</span></span> |



 

<span data-ttu-id="6c934-129">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6c934-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="6c934-130">Componente</span><span class="sxs-lookup"><span data-stu-id="6c934-130">Component</span></span>  | <span data-ttu-id="6c934-131">KeyPath</span><span class="sxs-lookup"><span data-stu-id="6c934-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="6c934-132">Component1</span><span class="sxs-lookup"><span data-stu-id="6c934-132">Component1</span></span> | <span data-ttu-id="6c934-133">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="6c934-133">File1</span></span>   |
| <span data-ttu-id="6c934-134">Component2</span><span class="sxs-lookup"><span data-stu-id="6c934-134">Component2</span></span> | <span data-ttu-id="6c934-135">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="6c934-135">File2</span></span>   |



 

[<span data-ttu-id="6c934-136">Tabela de ícones</span><span class="sxs-lookup"><span data-stu-id="6c934-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="6c934-137">Nome</span><span class="sxs-lookup"><span data-stu-id="6c934-137">Name</span></span>      | <span data-ttu-id="6c934-138">Dados</span><span class="sxs-lookup"><span data-stu-id="6c934-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="6c934-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="6c934-139">Icon1.bat</span></span> | <span data-ttu-id="6c934-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="6c934-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="6c934-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="6c934-141">Icon2.dat</span></span> | <span data-ttu-id="6c934-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="6c934-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="6c934-143">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6c934-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="6c934-144">Atalho</span><span class="sxs-lookup"><span data-stu-id="6c934-144">Shortcut</span></span>  | <span data-ttu-id="6c934-145">Componente</span><span class="sxs-lookup"><span data-stu-id="6c934-145">Component</span></span>  | <span data-ttu-id="6c934-146">Destino</span><span class="sxs-lookup"><span data-stu-id="6c934-146">Target</span></span>   | <span data-ttu-id="6c934-147">ícone\_</span><span class="sxs-lookup"><span data-stu-id="6c934-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="6c934-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="6c934-148">Shortcut1</span></span> | <span data-ttu-id="6c934-149">Component1</span><span class="sxs-lookup"><span data-stu-id="6c934-149">Component1</span></span> | <span data-ttu-id="6c934-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="6c934-150">Feature1</span></span> | <span data-ttu-id="6c934-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="6c934-151">Icon1.bat</span></span> |
| <span data-ttu-id="6c934-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="6c934-152">Shortcut2</span></span> | <span data-ttu-id="6c934-153">Component2</span><span class="sxs-lookup"><span data-stu-id="6c934-153">Component2</span></span> | <span data-ttu-id="6c934-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="6c934-154">Feature1</span></span> | <span data-ttu-id="6c934-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="6c934-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6c934-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c934-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c934-157">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6c934-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




