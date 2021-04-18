---
description: ICE32 valida que chaves e chaves estrangeiras no arquivo. msi são do mesmo tamanho e tipos de definição de coluna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753447"
---
# <a name="ice32"></a><span data-ttu-id="faf0e-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="faf0e-103">ICE32</span></span>

<span data-ttu-id="faf0e-104">ICE32 valida que chaves e chaves estrangeiras no arquivo. msi são do mesmo tamanho e tipos de definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="faf0e-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="faf0e-105">Essa ação personalizada de ICE faz a comparação usando a [ \_ tabela de validação](-validation-table.md) e usando os tipos de definição que são retornados por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span><span class="sxs-lookup"><span data-stu-id="faf0e-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="faf0e-106">Para obter mais informações, consulte [formato de definição de coluna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="faf0e-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="faf0e-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="faf0e-107">Result</span></span>

<span data-ttu-id="faf0e-108">O ICE32 posta erros se o arquivo. msi contém quaisquer chaves estrangeiras para chaves de um tipo de dados de coluna ou comprimento de coluna diferente.</span><span class="sxs-lookup"><span data-stu-id="faf0e-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="faf0e-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="faf0e-109">Example</span></span>

<span data-ttu-id="faf0e-110">ICE32 posta dois erros para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="faf0e-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="faf0e-111">Há uma chave estrangeira e uma chave definida que diferem no tamanho.</span><span class="sxs-lookup"><span data-stu-id="faf0e-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="faf0e-112">Há uma chave estrangeira e uma chave definida que diferem em seu tipo de definição.</span><span class="sxs-lookup"><span data-stu-id="faf0e-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="faf0e-113">[ \_ Tabela de validação](-validation-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="faf0e-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="faf0e-114">Tabela</span><span class="sxs-lookup"><span data-stu-id="faf0e-114">Table</span></span> | <span data-ttu-id="faf0e-115">Coluna</span><span class="sxs-lookup"><span data-stu-id="faf0e-115">Column</span></span>  | <span data-ttu-id="faf0e-116">KeyTable</span><span class="sxs-lookup"><span data-stu-id="faf0e-116">KeyTable</span></span> | <span data-ttu-id="faf0e-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="faf0e-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="faf0e-118">Arquivo</span><span class="sxs-lookup"><span data-stu-id="faf0e-118">File</span></span>  | <span data-ttu-id="faf0e-119">Versão</span><span class="sxs-lookup"><span data-stu-id="faf0e-119">Version</span></span> | <span data-ttu-id="faf0e-120">Arquivo</span><span class="sxs-lookup"><span data-stu-id="faf0e-120">File</span></span>     | <span data-ttu-id="faf0e-121">1</span><span class="sxs-lookup"><span data-stu-id="faf0e-121">1</span></span>         |
| <span data-ttu-id="faf0e-122">Oscila</span><span class="sxs-lookup"><span data-stu-id="faf0e-122">Flap</span></span>  | <span data-ttu-id="faf0e-123">Coluna8</span><span class="sxs-lookup"><span data-stu-id="faf0e-123">Column8</span></span> | <span data-ttu-id="faf0e-124">Oscila</span><span class="sxs-lookup"><span data-stu-id="faf0e-124">Flap</span></span>     | <span data-ttu-id="faf0e-125">1</span><span class="sxs-lookup"><span data-stu-id="faf0e-125">1</span></span>         |



 

<span data-ttu-id="faf0e-126">Definições de coluna (parcial)</span><span class="sxs-lookup"><span data-stu-id="faf0e-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="faf0e-127">Tabela</span><span class="sxs-lookup"><span data-stu-id="faf0e-127">Table</span></span> | <span data-ttu-id="faf0e-128">Coluna</span><span class="sxs-lookup"><span data-stu-id="faf0e-128">Column</span></span>  | <span data-ttu-id="faf0e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf0e-129">Type</span></span> | <span data-ttu-id="faf0e-130">Tamanho</span><span class="sxs-lookup"><span data-stu-id="faf0e-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="faf0e-131">Arquivo</span><span class="sxs-lookup"><span data-stu-id="faf0e-131">File</span></span>  | <span data-ttu-id="faf0e-132">Arquivo</span><span class="sxs-lookup"><span data-stu-id="faf0e-132">File</span></span>    | <span data-ttu-id="faf0e-133">s</span><span class="sxs-lookup"><span data-stu-id="faf0e-133">s</span></span>    | <span data-ttu-id="faf0e-134">72</span><span class="sxs-lookup"><span data-stu-id="faf0e-134">72</span></span>   |
| <span data-ttu-id="faf0e-135">Arquivo</span><span class="sxs-lookup"><span data-stu-id="faf0e-135">File</span></span>  | <span data-ttu-id="faf0e-136">Versão</span><span class="sxs-lookup"><span data-stu-id="faf0e-136">Version</span></span> | <span data-ttu-id="faf0e-137">S</span><span class="sxs-lookup"><span data-stu-id="faf0e-137">S</span></span>    | <span data-ttu-id="faf0e-138">32</span><span class="sxs-lookup"><span data-stu-id="faf0e-138">32</span></span>   |
| <span data-ttu-id="faf0e-139">Oscila</span><span class="sxs-lookup"><span data-stu-id="faf0e-139">Flap</span></span>  | <span data-ttu-id="faf0e-140">Column1</span><span class="sxs-lookup"><span data-stu-id="faf0e-140">Column1</span></span> | <span data-ttu-id="faf0e-141">i</span><span class="sxs-lookup"><span data-stu-id="faf0e-141">i</span></span>    | <span data-ttu-id="faf0e-142">2</span><span class="sxs-lookup"><span data-stu-id="faf0e-142">2</span></span>    |
| <span data-ttu-id="faf0e-143">Oscila</span><span class="sxs-lookup"><span data-stu-id="faf0e-143">Flap</span></span>  | <span data-ttu-id="faf0e-144">Coluna8</span><span class="sxs-lookup"><span data-stu-id="faf0e-144">Column8</span></span> | <span data-ttu-id="faf0e-145">S</span><span class="sxs-lookup"><span data-stu-id="faf0e-145">S</span></span>    | <span data-ttu-id="faf0e-146">32</span><span class="sxs-lookup"><span data-stu-id="faf0e-146">32</span></span>   |



 

<span data-ttu-id="faf0e-147">A coluna versão da tabela de arquivos pode ser uma chave estrangeira para outro arquivo na tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="faf0e-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="faf0e-148">Isso ocorre com arquivos complementares.</span><span class="sxs-lookup"><span data-stu-id="faf0e-148">This occurs with companion files.</span></span> <span data-ttu-id="faf0e-149">No entanto, a coluna Version só permite um comprimento de cadeia de caracteres 32, enquanto a coluna File permite um comprimento de cadeia de caracteres 72.</span><span class="sxs-lookup"><span data-stu-id="faf0e-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="faf0e-150">Para corrigir esse erro, altere os comprimentos da cadeia de caracteres para correspondência.</span><span class="sxs-lookup"><span data-stu-id="faf0e-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="faf0e-151">Há uma chave estrangeira e uma chave definida que diferem em seus tipos de definição.</span><span class="sxs-lookup"><span data-stu-id="faf0e-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="faf0e-152">Column8 da tabela de flap é listada como uma chave estrangeira para column1.</span><span class="sxs-lookup"><span data-stu-id="faf0e-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="faf0e-153">Column8 é uma coluna de cadeia de caracteres e column1 é uma coluna de inteiros.</span><span class="sxs-lookup"><span data-stu-id="faf0e-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="faf0e-154">Os pares chave estrangeira e chave devem ser definidos para que seus tipos de dados sejam correspondentes.</span><span class="sxs-lookup"><span data-stu-id="faf0e-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faf0e-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="faf0e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf0e-156">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="faf0e-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



