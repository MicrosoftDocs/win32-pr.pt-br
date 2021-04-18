---
description: ICE76 verifica o uso do catálogo SFP (WFP) em pacotes Windows Installer para Windows me. Essa ICE também verifica se nenhum arquivo na tabela BindImage referencia catálogos SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752043"
---
# <a name="ice76"></a><span data-ttu-id="d963b-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="d963b-104">ICE76</span></span>

<span data-ttu-id="d963b-105">ICE76 verifica o uso do catálogo SFP (WFP) em pacotes Windows Installer para Windows me.</span><span class="sxs-lookup"><span data-stu-id="d963b-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="d963b-106">Essa ICE também verifica se nenhum arquivo na [tabela](bindimage-table.md) BindImage referencia catálogos SFP.</span><span class="sxs-lookup"><span data-stu-id="d963b-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="d963b-107">A proteção de arquivos do Windows requer uma correspondência exata entre o arquivo e a assinatura inserida no arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="d963b-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="d963b-108">Os arquivos que fazem referência a um catálogo do SFP não devem ser listados na tabela BindImage porque o efeito da [ação de BindImage](bindimage-action.md) nesses arquivos é diferente entre os computadores.</span><span class="sxs-lookup"><span data-stu-id="d963b-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="d963b-109">Os arquivos referenciados por catálogos do SFP devem estar em componentes que são permanentes ou instalados localmente.</span><span class="sxs-lookup"><span data-stu-id="d963b-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="d963b-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="d963b-110">Result</span></span>

<span data-ttu-id="d963b-111">ICE76 posta um erro para cada arquivo na [tabela BindImage](bindimage-table.md) que também está na [tabela FileSFPCatalog](filesfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="d963b-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="d963b-112">ICE76 gera um erro se um arquivo na tabela FileSFPCatalog pertencer a um componente com qualquer um dos seguintes verdadeiros:</span><span class="sxs-lookup"><span data-stu-id="d963b-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="d963b-113">**msidbComponentAttributesPermanent** não está definido na coluna Attributes da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d963b-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="d963b-114">**msidbComponentAttributesSourceOnly** é definido na coluna Attributes da tabela Component.</span><span class="sxs-lookup"><span data-stu-id="d963b-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="d963b-115">**msidbAttributesOptional** é definido na coluna Attributes da tabela Component.</span><span class="sxs-lookup"><span data-stu-id="d963b-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="d963b-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d963b-116">Example</span></span>

<span data-ttu-id="d963b-117">ICE76 relata o seguinte erro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="d963b-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="d963b-118">[Tabela FileSFPCatalog](filesfpcatalog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d963b-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="d963b-119">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="d963b-119">File\_</span></span> | <span data-ttu-id="d963b-120">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="d963b-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="d963b-121">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="d963b-121">File1</span></span>  | <span data-ttu-id="d963b-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="d963b-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="d963b-123">[Tabela BindImage](bindimage-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d963b-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="d963b-124">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="d963b-124">File\_</span></span> |
|--------|
| <span data-ttu-id="d963b-125">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="d963b-125">File1</span></span>  |



 

<span data-ttu-id="d963b-126">Para corrigir isso, não insira nenhum arquivo que referencie catálogos SFP na tabela BindImage.</span><span class="sxs-lookup"><span data-stu-id="d963b-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d963b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d963b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d963b-128">Tabela BindImage</span><span class="sxs-lookup"><span data-stu-id="d963b-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="d963b-129">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="d963b-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="d963b-130">Tabela FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="d963b-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="d963b-131">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="d963b-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



