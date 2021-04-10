---
description: ICEM11 verifica se um módulo de mesclagem configurável lista a Tabela ModuleConfiguration e a tabela ModuleSubstitution na tabela ModuleIgnoreTable do módulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170428"
---
# <a name="icem11"></a><span data-ttu-id="b478f-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="b478f-103">ICEM11</span></span>

<span data-ttu-id="b478f-104">ICEM11 verifica se um módulo de mesclagem configurável lista a [Tabela ModuleConfiguration](moduleconfiguration-table.md) e a [tabela ModuleSubstitution](modulesubstitution-table.md) na [tabela ModuleIgnoreTable](moduleignoretable-table.md) do módulo.</span><span class="sxs-lookup"><span data-stu-id="b478f-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="b478f-105">Isso garante que as ferramentas de mesclagem que não reconheçam módulos de mesclagem configuráveis (menos que a versão 2,0) não copiem essas tabelas no banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="b478f-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="b478f-106">Esse ICEM está disponível no arquivo Mergemod. Cub fornecido no SDK do Windows Installer 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="b478f-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="b478f-107">Para obter detalhes, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b478f-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="b478f-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="b478f-108">Result</span></span>

<span data-ttu-id="b478f-109">ICEM11 lançará um erro se o módulo contiver uma tabela ModuleConfiguration ou ModuleSubstitution não listada na tabela ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="b478f-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="b478f-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b478f-110">Example</span></span>

<span data-ttu-id="b478f-111">ICEM11 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="b478f-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="b478f-112">[ModuleConfiguration](moduleconfiguration-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b478f-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="b478f-113">Nome</span><span class="sxs-lookup"><span data-stu-id="b478f-113">Name</span></span>     | <span data-ttu-id="b478f-114">Formatar</span><span class="sxs-lookup"><span data-stu-id="b478f-114">Format</span></span> | <span data-ttu-id="b478f-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="b478f-115">Type</span></span>   | <span data-ttu-id="b478f-116">ContextData</span><span class="sxs-lookup"><span data-stu-id="b478f-116">ContextData</span></span> | <span data-ttu-id="b478f-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b478f-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="b478f-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="b478f-118">IconKey1</span></span> | <span data-ttu-id="b478f-119">1</span><span class="sxs-lookup"><span data-stu-id="b478f-119">1</span></span>      | <span data-ttu-id="b478f-120">Binário</span><span class="sxs-lookup"><span data-stu-id="b478f-120">Binary</span></span> | <span data-ttu-id="b478f-121">ícone</span><span class="sxs-lookup"><span data-stu-id="b478f-121">Icon</span></span>        | <span data-ttu-id="b478f-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="b478f-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="b478f-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="b478f-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="b478f-124">Tabela</span><span class="sxs-lookup"><span data-stu-id="b478f-124">Table</span></span>   | <span data-ttu-id="b478f-125">Linha</span><span class="sxs-lookup"><span data-stu-id="b478f-125">Row</span></span>              | <span data-ttu-id="b478f-126">Coluna</span><span class="sxs-lookup"><span data-stu-id="b478f-126">Column</span></span> | <span data-ttu-id="b478f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b478f-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="b478f-128">Control</span><span class="sxs-lookup"><span data-stu-id="b478f-128">Control</span></span> | <span data-ttu-id="b478f-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="b478f-129">Dialog1;Control1</span></span> | <span data-ttu-id="b478f-130">Texto</span><span class="sxs-lookup"><span data-stu-id="b478f-130">Text</span></span>   | <span data-ttu-id="b478f-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="b478f-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="b478f-132">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="b478f-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="b478f-133">Tabela</span><span class="sxs-lookup"><span data-stu-id="b478f-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="b478f-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b478f-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="b478f-135">Para corrigir esse erro, inclua as tabelas ModuleSubstitution e ModuleConfiguration na tabela ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="b478f-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="b478f-136">Tabela usada durante a execução</span><span class="sxs-lookup"><span data-stu-id="b478f-136">Table Used During Execution</span></span>

[<span data-ttu-id="b478f-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="b478f-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="b478f-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b478f-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="b478f-139">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="b478f-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="b478f-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b478f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b478f-141">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="b478f-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



