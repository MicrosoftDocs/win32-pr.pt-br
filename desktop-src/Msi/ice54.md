---
description: O ICE54 verifica os componentes que usam um arquivo complementar como seu caminho de chave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828568"
---
# <a name="ice54"></a><span data-ttu-id="95154-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="95154-103">ICE54</span></span>

<span data-ttu-id="95154-104">O ICE54 verifica os componentes que usam um arquivo complementar como seu caminho de chave.</span><span class="sxs-lookup"><span data-stu-id="95154-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="95154-105">O arquivo de caminho de chave de um componente não deve derivar sua versão de um arquivo diferente.</span><span class="sxs-lookup"><span data-stu-id="95154-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="95154-106">Isso pode fazer com que alguns arquivos falhem na instalação.</span><span class="sxs-lookup"><span data-stu-id="95154-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="95154-107">Consulte a [tabela de arquivos](file-table.md) para obter mais informações sobre arquivos complementares.</span><span class="sxs-lookup"><span data-stu-id="95154-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="95154-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="95154-108">Result</span></span>

<span data-ttu-id="95154-109">ICE54 posta um aviso se algum componente tiver um arquivo de caminho de chave que derive sua versão de outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="95154-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="95154-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="95154-110">Example</span></span>

<span data-ttu-id="95154-111">ICE54 retorna o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="95154-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="95154-112">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="95154-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="95154-113">Componente</span><span class="sxs-lookup"><span data-stu-id="95154-113">Component</span></span>  | <span data-ttu-id="95154-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="95154-114">Attribute</span></span> | <span data-ttu-id="95154-115">KeyPath</span><span class="sxs-lookup"><span data-stu-id="95154-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="95154-116">Component1</span><span class="sxs-lookup"><span data-stu-id="95154-116">Component1</span></span> | <span data-ttu-id="95154-117">0</span><span class="sxs-lookup"><span data-stu-id="95154-117">0</span></span>         | <span data-ttu-id="95154-118">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="95154-118">File1</span></span>   |



 

<span data-ttu-id="95154-119">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="95154-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="95154-120">Arquivo</span><span class="sxs-lookup"><span data-stu-id="95154-120">File</span></span>  | <span data-ttu-id="95154-121">Versão</span><span class="sxs-lookup"><span data-stu-id="95154-121">Version</span></span> | <span data-ttu-id="95154-122">Idioma</span><span class="sxs-lookup"><span data-stu-id="95154-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="95154-123">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="95154-123">File1</span></span> | <span data-ttu-id="95154-124">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="95154-124">File2</span></span>   |          |
| <span data-ttu-id="95154-125">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="95154-125">File2</span></span> | <span data-ttu-id="95154-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="95154-126">1.0.0.0</span></span> | <span data-ttu-id="95154-127">1046</span><span class="sxs-lookup"><span data-stu-id="95154-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="95154-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95154-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95154-129">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="95154-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



