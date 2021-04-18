---
description: O ICE48 verifica os diretórios que são embutidos em código para caminhos locais na tabela de propriedades.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787500"
---
# <a name="ice48"></a><span data-ttu-id="2cb48-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="2cb48-103">ICE48</span></span>

<span data-ttu-id="2cb48-104">O ICE48 verifica os diretórios que são embutidos em código para caminhos locais na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2cb48-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="2cb48-105">Não codifique caminhos de diretório para unidades locais porque computadores diferem na configuração da unidade local.</span><span class="sxs-lookup"><span data-stu-id="2cb48-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="2cb48-106">Essa prática pode ser aceitável se estiver implantando um aplicativo em um grande número de computadores nos quais as partes relevantes das unidades são todas iguais.</span><span class="sxs-lookup"><span data-stu-id="2cb48-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="2cb48-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="2cb48-107">Result</span></span>

<span data-ttu-id="2cb48-108">ICE48 posta uma mensagem de erro se houver um diretório embutido em código para um caminho local na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2cb48-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="2cb48-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2cb48-109">Example</span></span>

<span data-ttu-id="2cb48-110">ICE48 relataria o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="2cb48-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="2cb48-111">[Tabela de diretórios](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2cb48-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="2cb48-112">Diretório</span><span class="sxs-lookup"><span data-stu-id="2cb48-112">Directory</span></span> | <span data-ttu-id="2cb48-113">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="2cb48-113">Directory\_Parent</span></span> | <span data-ttu-id="2cb48-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="2cb48-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="2cb48-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="2cb48-115">Dir1</span></span>      |                   | <span data-ttu-id="2cb48-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="2cb48-116">SourceDir</span></span>  |



 

<span data-ttu-id="2cb48-117">[Tabela de propriedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2cb48-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="2cb48-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2cb48-118">Property</span></span> | <span data-ttu-id="2cb48-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2cb48-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="2cb48-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="2cb48-120">Dir1</span></span>     | <span data-ttu-id="2cb48-121">d: \\ origem</span><span class="sxs-lookup"><span data-stu-id="2cb48-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2cb48-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cb48-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cb48-123">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="2cb48-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



