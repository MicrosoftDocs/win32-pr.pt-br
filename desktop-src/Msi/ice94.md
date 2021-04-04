---
description: ICE94 verifica a tabela de atalho, a tabela de recursos e a tabela MsiAssembly e posta um aviso se houver algum atalho não anunciado apontando para um arquivo de assembly no cache de assembly global.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171139"
---
# <a name="ice94"></a><span data-ttu-id="56455-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="56455-103">ICE94</span></span>

<span data-ttu-id="56455-104">ICE94 verifica a [tabela de atalho](shortcut-table.md), a [tabela de recursos](feature-table.md)e a [tabela MsiAssembly](msiassembly-table.md) e posta um aviso se houver algum atalho não anunciado apontando para um arquivo de assembly no cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="56455-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="56455-105">Se a entrada no campo destino da tabela de atalho não for um recurso na tabela de recursos, o atalho será desanunciado.</span><span class="sxs-lookup"><span data-stu-id="56455-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="56455-106">Se a entrada no campo componente \_ da tabela de atalho também estiver listada na tabela MsiAssembly, o atalho apontará para um arquivo de assembly.</span><span class="sxs-lookup"><span data-stu-id="56455-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="56455-107">Se a entrada no \_ campo aplicativo de arquivo na tabela MsiAssembly estiver vazia, o arquivo de assembly estará no cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="56455-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="56455-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="56455-108">Result</span></span>

<span data-ttu-id="56455-109">ICE94 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="56455-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="56455-110">Aviso de ICE94</span><span class="sxs-lookup"><span data-stu-id="56455-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="56455-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="56455-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56455-112">O atalho não anunciado ' \[ 2 \] ' aponta para um arquivo de assembly no cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="56455-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="56455-113">Um atalho não anunciado está apontando para um arquivo de assembly no cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="56455-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="56455-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="56455-114">Example</span></span>

<span data-ttu-id="56455-115">ICE94 relata o seguinte erro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="56455-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="56455-116">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="56455-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="56455-117">Atalho</span><span class="sxs-lookup"><span data-stu-id="56455-117">Shortcut</span></span>  | <span data-ttu-id="56455-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="56455-118">Component\_</span></span> | <span data-ttu-id="56455-119">Destino</span><span class="sxs-lookup"><span data-stu-id="56455-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="56455-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="56455-120">shortcut1</span></span> | <span data-ttu-id="56455-121">c1</span><span class="sxs-lookup"><span data-stu-id="56455-121">c1</span></span>          | <span data-ttu-id="56455-122">\[arquivo1\]</span><span class="sxs-lookup"><span data-stu-id="56455-122">\[file1\]</span></span> |
| <span data-ttu-id="56455-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="56455-123">shortcut2</span></span> | <span data-ttu-id="56455-124">c2</span><span class="sxs-lookup"><span data-stu-id="56455-124">c2</span></span>          | <span data-ttu-id="56455-125">feature1</span><span class="sxs-lookup"><span data-stu-id="56455-125">feature1</span></span>  |
| <span data-ttu-id="56455-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="56455-126">shortcut3</span></span> | <span data-ttu-id="56455-127">c3</span><span class="sxs-lookup"><span data-stu-id="56455-127">c3</span></span>          | <span data-ttu-id="56455-128">\[file2\]</span><span class="sxs-lookup"><span data-stu-id="56455-128">\[file2\]</span></span> |



 

<span data-ttu-id="56455-129">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="56455-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="56455-130">Recurso</span><span class="sxs-lookup"><span data-stu-id="56455-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="56455-131">feature1</span><span class="sxs-lookup"><span data-stu-id="56455-131">feature1</span></span> |



 

<span data-ttu-id="56455-132">[Tabela MsiAssembly](msiassembly-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="56455-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="56455-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="56455-133">Component\_</span></span> | <span data-ttu-id="56455-134">Aplicativo de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="56455-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="56455-135">c1</span><span class="sxs-lookup"><span data-stu-id="56455-135">c1</span></span>          |                   |
| <span data-ttu-id="56455-136">c2</span><span class="sxs-lookup"><span data-stu-id="56455-136">c2</span></span>          |                   |
| <span data-ttu-id="56455-137">c3</span><span class="sxs-lookup"><span data-stu-id="56455-137">c3</span></span>          | <span data-ttu-id="56455-138">fa1</span><span class="sxs-lookup"><span data-stu-id="56455-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="56455-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56455-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56455-140">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="56455-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



