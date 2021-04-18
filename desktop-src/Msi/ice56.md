---
description: ICE56 valida que a estrutura de diretório do arquivo. msi tem um único diretório raiz, que a raiz é a propriedade TARGETDIR e que o valor da propriedade SourceDir está na coluna DefaultDir da tabela de diretórios.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753263"
---
# <a name="ice56"></a><span data-ttu-id="58e81-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="58e81-103">ICE56</span></span>

<span data-ttu-id="58e81-104">ICE56 valida que a estrutura de diretório do arquivo. msi tem um único diretório raiz, que a raiz é a propriedade [**TARGETDIR**](targetdir.md) e que o valor da propriedade [**SourceDir**](sourcedir.md) está na coluna DefaultDir da [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="58e81-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="58e81-105">Se um arquivo. msi tiver várias raízes ou especificar uma raiz diferente de [**TARGETDIR**](targetdir.md), uma [instalação administrativa](administrative-installation.md) não criará uma imagem administrativa correta.</span><span class="sxs-lookup"><span data-stu-id="58e81-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="58e81-106">Observe que os diretórios vazios não são verificados por ICE56.</span><span class="sxs-lookup"><span data-stu-id="58e81-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="58e81-107">A estrutura de diretório passa a validação com vários diretórios raiz se os diretórios extras estiverem vazios.</span><span class="sxs-lookup"><span data-stu-id="58e81-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="58e81-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="58e81-108">Result</span></span>

<span data-ttu-id="58e81-109">ICE56 lançará um erro se o. msi não tiver uma única raiz, [**TARGETDIR**](targetdir.md)ou se [**SourceDir**](sourcedir.md) não estiver especificado na coluna DefaultDir da [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="58e81-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="58e81-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="58e81-110">Example</span></span>

<span data-ttu-id="58e81-111">ICE56 relata os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="58e81-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="58e81-112">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="58e81-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="58e81-113">Diretório</span><span class="sxs-lookup"><span data-stu-id="58e81-113">Directory</span></span> | <span data-ttu-id="58e81-114">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="58e81-114">Directory\_Parent</span></span> | <span data-ttu-id="58e81-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="58e81-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="58e81-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="58e81-116">TARGETDIR</span></span> |                   | <span data-ttu-id="58e81-117">Temp</span><span class="sxs-lookup"><span data-stu-id="58e81-117">Temp</span></span>       |
| <span data-ttu-id="58e81-118">Root2</span><span class="sxs-lookup"><span data-stu-id="58e81-118">Root2</span></span>     | <span data-ttu-id="58e81-119">Root2</span><span class="sxs-lookup"><span data-stu-id="58e81-119">Root2</span></span>             | <span data-ttu-id="58e81-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="58e81-120">SourceDir</span></span>  |



 

<span data-ttu-id="58e81-121">Para corrigir o primeiro erro, a raiz [**TARGETDIR**](targetdir.md) deve ter um valor DefaultDir de [**SourceDir**](sourcedir.md).</span><span class="sxs-lookup"><span data-stu-id="58e81-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="58e81-122">SOURCEDIR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="58e81-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="58e81-123">Pode ser possível tornar **TARGETDIR** o pai da segunda raiz e usar o valor '. ' na coluna DefaultDir.</span><span class="sxs-lookup"><span data-stu-id="58e81-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="58e81-124">Consulte a [tabela de diretórios](directory-table.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="58e81-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="58e81-125">Para corrigir o segundo erro, a estrutura de diretório deve ter apenas uma raiz chamada [**TARGETDIR**](targetdir.md).</span><span class="sxs-lookup"><span data-stu-id="58e81-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58e81-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58e81-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e81-127">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="58e81-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



