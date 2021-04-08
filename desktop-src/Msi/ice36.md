---
description: ICE36 valida que cada ícone na tabela de ícones é listado pelo menos uma vez na propriedade ARPPRODUCTICON ou nas tabelas de classe, ProgId ou atalho.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011296"
---
# <a name="ice36"></a><span data-ttu-id="99966-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="99966-103">ICE36</span></span>

<span data-ttu-id="99966-104">ICE36 valida que cada ícone na tabela de ícones é listado pelo menos uma vez na propriedade [**ARPPRODUCTICON**](arpproducticon.md) ou nas tabelas de [classe](class-table.md), [ProgID](progid-table.md)ou [atalho](shortcut-table.md) .</span><span class="sxs-lookup"><span data-stu-id="99966-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="99966-105">Durante o anúncio, o instalador instala todos os ícones listados na [tabela de ícones](icon-table.md) no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="99966-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="99966-106">Ter ícones não utilizados na tabela de ícones não impede que a instalação seja executada, no entanto, ele aumenta desnecessariamente o tamanho do arquivo. msi e a hora e o espaço necessários para anunciar um recurso.</span><span class="sxs-lookup"><span data-stu-id="99966-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="99966-107">Se um ícone não for referenciado na propriedade ou tabela e não houver interface do usuário fornecida para criar uma referência em tempo de execução, você deverá remover o ícone para obter um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="99966-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="99966-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="99966-108">Result</span></span>

<span data-ttu-id="99966-109">ICE36 posta uma mensagem se houver um ícone na tabela de ícones que não é referenciado nas tabelas de [classe](class-table.md), [ProgID](progid-table.md)ou [atalho](shortcut-table.md) e se não houver nenhuma interface do usuário fornecida para criar essa referência em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="99966-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="99966-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="99966-110">Example</span></span>

<span data-ttu-id="99966-111">ICE36 relata o seguinte erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="99966-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="99966-112">[Tabela de ícones](icon-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="99966-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="99966-113">Nome</span><span class="sxs-lookup"><span data-stu-id="99966-113">Name</span></span>  | <span data-ttu-id="99966-114">Dados</span><span class="sxs-lookup"><span data-stu-id="99966-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="99966-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="99966-115">Icon1</span></span> | <span data-ttu-id="99966-116">Control1</span><span class="sxs-lookup"><span data-stu-id="99966-116">Control1</span></span> |
| <span data-ttu-id="99966-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="99966-117">Icon2</span></span> | <span data-ttu-id="99966-118">Control2</span><span class="sxs-lookup"><span data-stu-id="99966-118">Control2</span></span> |
| <span data-ttu-id="99966-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="99966-119">Icon3</span></span> | <span data-ttu-id="99966-120">Control3</span><span class="sxs-lookup"><span data-stu-id="99966-120">Control3</span></span> |
| <span data-ttu-id="99966-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="99966-121">Icon4</span></span> | <span data-ttu-id="99966-122">Control4</span><span class="sxs-lookup"><span data-stu-id="99966-122">Control4</span></span> |



 

<span data-ttu-id="99966-123">[Tabela ProgID](progid-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="99966-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="99966-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="99966-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="99966-125">Property1</span><span class="sxs-lookup"><span data-stu-id="99966-125">Property1</span></span> |



 

<span data-ttu-id="99966-126">[Tabela de classes](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="99966-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="99966-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="99966-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="99966-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="99966-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="99966-129">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="99966-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="99966-130">Atalho</span><span class="sxs-lookup"><span data-stu-id="99966-130">Shortcut</span></span>  | <span data-ttu-id="99966-131">ícone\_</span><span class="sxs-lookup"><span data-stu-id="99966-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="99966-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="99966-132">Shortcut1</span></span> | <span data-ttu-id="99966-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="99966-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="99966-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99966-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99966-135">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="99966-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



