---
description: ICE02 valida que determinadas referências entre o componente, o arquivo e as tabelas do registro são recíprocas. Essas referências devem ser recíprocas para que o instalador determine corretamente o estado de instalação dos componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646808"
---
# <a name="ice02"></a><span data-ttu-id="6e73c-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="6e73c-104">ICE02</span></span>

<span data-ttu-id="6e73c-105">ICE02 valida que determinadas referências entre o [componente](component-table.md), o [arquivo](file-table.md)e as tabelas [do registro](registry-table.md) são recíprocas.</span><span class="sxs-lookup"><span data-stu-id="6e73c-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="6e73c-106">Essas referências devem ser recíprocas para que o instalador determine corretamente o estado de instalação dos componentes.</span><span class="sxs-lookup"><span data-stu-id="6e73c-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="6e73c-107">O instalador usa a coluna KeyPath da tabela de componentes para detectar a presença do componente listado na coluna componente.</span><span class="sxs-lookup"><span data-stu-id="6e73c-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="6e73c-108">A coluna KeyPath contém uma chave para as tabelas de arquivo ou registro.</span><span class="sxs-lookup"><span data-stu-id="6e73c-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="6e73c-109">Ambas as tabelas têm uma coluna de componente \_ que contém uma chave de volta para a tabela de componentes apontando para o componente que controla a entrada ou o arquivo do registro.</span><span class="sxs-lookup"><span data-stu-id="6e73c-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="6e73c-110">Essas referências devem ser recíprocas.</span><span class="sxs-lookup"><span data-stu-id="6e73c-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="6e73c-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="6e73c-111">Result</span></span>

<span data-ttu-id="6e73c-112">ICE02 posta uma mensagem de erro se encontrar uma referência que deve ser recíproca e não.</span><span class="sxs-lookup"><span data-stu-id="6e73c-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="6e73c-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6e73c-113">Example</span></span>

<span data-ttu-id="6e73c-114">ICE02 publicaria a seguinte mensagem de erro para um arquivo. msi que contém as entradas de banco de dados mostradas.</span><span class="sxs-lookup"><span data-stu-id="6e73c-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="6e73c-115">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6e73c-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="6e73c-116">Componente</span><span class="sxs-lookup"><span data-stu-id="6e73c-116">Component</span></span> | <span data-ttu-id="6e73c-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="6e73c-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="6e73c-118">Vermelho</span><span class="sxs-lookup"><span data-stu-id="6e73c-118">Red</span></span>       | <span data-ttu-id="6e73c-119">\_Arquivo vermelho</span><span class="sxs-lookup"><span data-stu-id="6e73c-119">Red\_File</span></span> |
| <span data-ttu-id="6e73c-120">Azul</span><span class="sxs-lookup"><span data-stu-id="6e73c-120">Blue</span></span>      | <span data-ttu-id="6e73c-121">\_Arquivo vermelho</span><span class="sxs-lookup"><span data-stu-id="6e73c-121">Red\_File</span></span> |



 

<span data-ttu-id="6e73c-122">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6e73c-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="6e73c-123">Coluna de arquivo</span><span class="sxs-lookup"><span data-stu-id="6e73c-123">File Column</span></span> | <span data-ttu-id="6e73c-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="6e73c-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="6e73c-125">\_Arquivo vermelho</span><span class="sxs-lookup"><span data-stu-id="6e73c-125">Red\_File</span></span>   | <span data-ttu-id="6e73c-126">Vermelho</span><span class="sxs-lookup"><span data-stu-id="6e73c-126">Red</span></span>         |
| <span data-ttu-id="6e73c-127">\_Arquivo azul</span><span class="sxs-lookup"><span data-stu-id="6e73c-127">Blue\_File</span></span>  | <span data-ttu-id="6e73c-128">Azul</span><span class="sxs-lookup"><span data-stu-id="6e73c-128">Blue</span></span>        |



 

<span data-ttu-id="6e73c-129">O componente Blue faz referência \_ a arquivo vermelho, mas \_ o arquivo vermelho não é controlado pelo componente azul e, portanto, não pode ser o arquivo KeyPath.</span><span class="sxs-lookup"><span data-stu-id="6e73c-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="6e73c-130">Se o instalador foi chamado para obter o estado de instalação de azul, ele verificaria incorretamente se o \_ arquivo vermelho foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6e73c-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="6e73c-131">A alteração do campo KeyPath para azul na tabela de componentes para \_ arquivo azul corrige o erro.</span><span class="sxs-lookup"><span data-stu-id="6e73c-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e73c-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e73c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e73c-133">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6e73c-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



