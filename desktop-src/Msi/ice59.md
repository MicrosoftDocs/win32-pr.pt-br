---
description: ICE59 verifica se os atalhos anunciados pertencem aos componentes instalados pelo recurso de destino do atalho.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752455"
---
# <a name="ice59"></a><span data-ttu-id="827b2-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="827b2-103">ICE59</span></span>

<span data-ttu-id="827b2-104">ICE59 verifica se os atalhos anunciados pertencem aos componentes instalados pelo recurso de destino do atalho.</span><span class="sxs-lookup"><span data-stu-id="827b2-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="827b2-105">Os erros relatados por ICE59 geralmente levam ao seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="827b2-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="827b2-106">O atalho anunciado iniciará o Windows Installer para instalar o recurso listado na coluna de destino.</span><span class="sxs-lookup"><span data-stu-id="827b2-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="827b2-107">Mas como a [tabela FeatureComponents](featurecomponents-table.md) não mapeia o recurso de destino para o componente que contém o atalho, o keyfile do componente (que é ativado pelo atalho) não é instalado.</span><span class="sxs-lookup"><span data-stu-id="827b2-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="827b2-108">Portanto, o atalho é quebrado e não fará nada.</span><span class="sxs-lookup"><span data-stu-id="827b2-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="827b2-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="827b2-109">Result</span></span>

<span data-ttu-id="827b2-110">ICE59 posta um erro se um atalho anunciado não pertencer aos componentes instalados pelo recurso de destino do atalho.</span><span class="sxs-lookup"><span data-stu-id="827b2-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="827b2-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="827b2-111">Example</span></span>

<span data-ttu-id="827b2-112">ICE59 relata o seguinte erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="827b2-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="827b2-113">Nesse caso, ShortcutB anuncia o recurso e, quando ativado, inicia o arquivo de chave de ComponentB.</span><span class="sxs-lookup"><span data-stu-id="827b2-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="827b2-114">Ainda assim, o ComponentB nunca é instalado pelo Recursoa, então mesmo após a fase de instalação sob demanda ser concluída, o destino do atalho não existe.</span><span class="sxs-lookup"><span data-stu-id="827b2-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="827b2-115">Para corrigir esse erro, adicione uma linha à [tabela FeatureComponents](featurecomponents-table.md) que associa o recurso e o ComponentB.</span><span class="sxs-lookup"><span data-stu-id="827b2-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="827b2-116">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="827b2-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="827b2-117">Atalho</span><span class="sxs-lookup"><span data-stu-id="827b2-117">Shortcut</span></span>  | <span data-ttu-id="827b2-118">Destino</span><span class="sxs-lookup"><span data-stu-id="827b2-118">Target</span></span>   | <span data-ttu-id="827b2-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="827b2-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="827b2-120">ShortcutB</span><span class="sxs-lookup"><span data-stu-id="827b2-120">ShortcutB</span></span> | <span data-ttu-id="827b2-121">Recurso</span><span class="sxs-lookup"><span data-stu-id="827b2-121">FeatureA</span></span> | <span data-ttu-id="827b2-122">ComponentB</span><span class="sxs-lookup"><span data-stu-id="827b2-122">ComponentB</span></span>  |



 

[<span data-ttu-id="827b2-123">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="827b2-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="827b2-124">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="827b2-124">Feature\_</span></span> | <span data-ttu-id="827b2-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="827b2-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="827b2-126">Recurso</span><span class="sxs-lookup"><span data-stu-id="827b2-126">FeatureA</span></span>  | <span data-ttu-id="827b2-127">Componente</span><span class="sxs-lookup"><span data-stu-id="827b2-127">ComponentA</span></span>  |



 

<span data-ttu-id="827b2-128">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="827b2-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="827b2-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="827b2-129">Feature</span></span>  | <span data-ttu-id="827b2-130">Nível</span><span class="sxs-lookup"><span data-stu-id="827b2-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="827b2-131">Recurso</span><span class="sxs-lookup"><span data-stu-id="827b2-131">FeatureA</span></span> | <span data-ttu-id="827b2-132">10</span><span class="sxs-lookup"><span data-stu-id="827b2-132">10</span></span>    |



 

<span data-ttu-id="827b2-133">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="827b2-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="827b2-134">Componente</span><span class="sxs-lookup"><span data-stu-id="827b2-134">Component</span></span>  | <span data-ttu-id="827b2-135">KeyPath</span><span class="sxs-lookup"><span data-stu-id="827b2-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="827b2-136">Componente</span><span class="sxs-lookup"><span data-stu-id="827b2-136">ComponentA</span></span> | <span data-ttu-id="827b2-137">FileA</span><span class="sxs-lookup"><span data-stu-id="827b2-137">FileA</span></span>   |
| <span data-ttu-id="827b2-138">ComponentB</span><span class="sxs-lookup"><span data-stu-id="827b2-138">ComponentB</span></span> | <span data-ttu-id="827b2-139">FileB</span><span class="sxs-lookup"><span data-stu-id="827b2-139">FileB</span></span>   |



 

<span data-ttu-id="827b2-140">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="827b2-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="827b2-141">Arquivo</span><span class="sxs-lookup"><span data-stu-id="827b2-141">File</span></span>  | <span data-ttu-id="827b2-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="827b2-142">Component\_</span></span> | <span data-ttu-id="827b2-143">Sequência</span><span class="sxs-lookup"><span data-stu-id="827b2-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="827b2-144">FileA</span><span class="sxs-lookup"><span data-stu-id="827b2-144">FileA</span></span> | <span data-ttu-id="827b2-145">Componente</span><span class="sxs-lookup"><span data-stu-id="827b2-145">ComponentA</span></span>  | <span data-ttu-id="827b2-146">1</span><span class="sxs-lookup"><span data-stu-id="827b2-146">1</span></span>        |
| <span data-ttu-id="827b2-147">FileB</span><span class="sxs-lookup"><span data-stu-id="827b2-147">FileB</span></span> | <span data-ttu-id="827b2-148">ComponentB</span><span class="sxs-lookup"><span data-stu-id="827b2-148">ComponentB</span></span>  | <span data-ttu-id="827b2-149">2</span><span class="sxs-lookup"><span data-stu-id="827b2-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="827b2-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="827b2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827b2-151">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="827b2-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



