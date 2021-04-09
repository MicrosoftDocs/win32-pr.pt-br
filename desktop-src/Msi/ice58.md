---
description: ICE58 verifica se a tabela de mídia não tem mais de 80 linhas.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922328"
---
# <a name="ice58"></a><span data-ttu-id="dd182-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="dd182-103">ICE58</span></span>

<span data-ttu-id="dd182-104">ICE58 verifica se a [tabela de mídia](media-table.md) não tem mais de 80 linhas.</span><span class="sxs-lookup"><span data-stu-id="dd182-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="dd182-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="dd182-105">Result</span></span>

<span data-ttu-id="dd182-106">Os avisos relatados pelo ICE58 causam falha na instalação, a menos que o pacote seja instalado com o Windows Installer 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dd182-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="dd182-107">A partir do Windows Installer 2,0, a restrição para mais de 80 entradas de tabela de mídia é removida.</span><span class="sxs-lookup"><span data-stu-id="dd182-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="dd182-108">Nenhum aviso será emitido se a propriedade de [**Resumo contagem de páginas**](page-count-summary.md) do pacote for maior ou igual a 150.</span><span class="sxs-lookup"><span data-stu-id="dd182-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="dd182-109">Os pacotes de esquema 200 ou superior só podem ser instalados pelo Windows Installer 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dd182-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="dd182-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dd182-110">Example</span></span>

<span data-ttu-id="dd182-111">ICE58 relata os erros e avisos a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="dd182-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="dd182-112">Para corrigir esse erro, elimine as entradas de tabela de mídia não utilizadas, consolide as entradas de tabela de mídia que se referem à mesma mídia e reempacote seu aplicativo para reduzir a mídia necessária.</span><span class="sxs-lookup"><span data-stu-id="dd182-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="dd182-113">[Tabela de mídia](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="dd182-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="dd182-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="dd182-114">DiskId</span></span> | <span data-ttu-id="dd182-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="dd182-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="dd182-116">1</span><span class="sxs-lookup"><span data-stu-id="dd182-116">1</span></span>      | <span data-ttu-id="dd182-117">10</span><span class="sxs-lookup"><span data-stu-id="dd182-117">10</span></span>             |
| <span data-ttu-id="dd182-118">2</span><span class="sxs-lookup"><span data-stu-id="dd182-118">2</span></span>      | <span data-ttu-id="dd182-119">20</span><span class="sxs-lookup"><span data-stu-id="dd182-119">20</span></span>             |
| <span data-ttu-id="dd182-120">...</span><span class="sxs-lookup"><span data-stu-id="dd182-120">...</span></span>    | <span data-ttu-id="dd182-121">...</span><span class="sxs-lookup"><span data-stu-id="dd182-121">...</span></span>            |
| <span data-ttu-id="dd182-122">81</span><span class="sxs-lookup"><span data-stu-id="dd182-122">81</span></span>     | <span data-ttu-id="dd182-123">810</span><span class="sxs-lookup"><span data-stu-id="dd182-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="dd182-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd182-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd182-125">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="dd182-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



