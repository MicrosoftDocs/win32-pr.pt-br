---
description: ICE52 verifica as propriedades particulares na tabela AppSearch. Consulte sobre propriedades.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829475"
---
# <a name="ice52"></a><span data-ttu-id="bf431-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="bf431-104">ICE52</span></span>

<span data-ttu-id="bf431-105">ICE52 verifica as propriedades particulares na [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="bf431-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="bf431-106">Consulte [sobre propriedades](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bf431-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="bf431-107">Ao usar o Windows 2000, todas as propriedades definidas na coluna propriedade da tabela AppSearch devem ser propriedades públicas.</span><span class="sxs-lookup"><span data-stu-id="bf431-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="bf431-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="bf431-108">Result</span></span>

<span data-ttu-id="bf431-109">ICE52 posta um aviso se houver uma propriedade privada na tabela AppSearch.</span><span class="sxs-lookup"><span data-stu-id="bf431-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="bf431-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf431-110">Example</span></span>

<span data-ttu-id="bf431-111">ICE52 posta o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="bf431-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="bf431-112">Tabela AppSearch</span><span class="sxs-lookup"><span data-stu-id="bf431-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="bf431-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bf431-113">Property</span></span>  | <span data-ttu-id="bf431-114">Assinatura</span><span class="sxs-lookup"><span data-stu-id="bf431-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="bf431-115">PROPERTY1</span><span class="sxs-lookup"><span data-stu-id="bf431-115">PROPERTY1</span></span> | <span data-ttu-id="bf431-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="bf431-116">Signature1</span></span> |
| <span data-ttu-id="bf431-117">Property2</span><span class="sxs-lookup"><span data-stu-id="bf431-117">Property2</span></span> | <span data-ttu-id="bf431-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="bf431-118">Signature2</span></span> |



 

<span data-ttu-id="bf431-119">Para corrigir esse aviso, altere para a propriedade pública personalizada: PROPERTY2.</span><span class="sxs-lookup"><span data-stu-id="bf431-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf431-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf431-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf431-121">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="bf431-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



