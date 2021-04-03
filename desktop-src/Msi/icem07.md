---
description: ICEM07 verifica se a ordem dos arquivos na tabela de sequência corresponde à ordem dos arquivos no MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828713"
---
# <a name="icem07"></a><span data-ttu-id="0f652-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="0f652-103">ICEM07</span></span>

<span data-ttu-id="0f652-104">ICEM07 verifica se a ordem dos arquivos na tabela de sequência corresponde à ordem dos arquivos no [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="0f652-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="0f652-105">O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="0f652-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="0f652-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="0f652-106">Result</span></span>

<span data-ttu-id="0f652-107">ICEM07 lançará um erro se a ordem dos arquivos na tabela de arquivos não corresponder à ordem no arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="0f652-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="0f652-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0f652-108">Example</span></span>

<span data-ttu-id="0f652-109">IC0M07 publicaria a seguinte mensagem de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="0f652-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="0f652-110">File Table</span><span class="sxs-lookup"><span data-stu-id="0f652-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="0f652-111">Arquivo</span><span class="sxs-lookup"><span data-stu-id="0f652-111">File</span></span>          | <span data-ttu-id="0f652-112">Sequência</span><span class="sxs-lookup"><span data-stu-id="0f652-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="0f652-113">FileA. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-113">FileA.*GUID1*</span></span> | <span data-ttu-id="0f652-114">1</span><span class="sxs-lookup"><span data-stu-id="0f652-114">1</span></span>        |
| <span data-ttu-id="0f652-115">FileB. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-115">FileB.*GUID1*</span></span> | <span data-ttu-id="0f652-116">8</span><span class="sxs-lookup"><span data-stu-id="0f652-116">8</span></span>        |
| <span data-ttu-id="0f652-117">FileC. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-117">FileC.*GUID1*</span></span> | <span data-ttu-id="0f652-118">52</span><span class="sxs-lookup"><span data-stu-id="0f652-118">52</span></span>       |



 

<span data-ttu-id="0f652-119">[MergeModule.CABda inet](mergemodule-cabinet.md) inserida</span><span class="sxs-lookup"><span data-stu-id="0f652-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="0f652-120">Arquivo</span><span class="sxs-lookup"><span data-stu-id="0f652-120">File</span></span>          |
|---------------|
| <span data-ttu-id="0f652-121">FileA. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="0f652-122">FileC. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="0f652-123">Arquiva. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="0f652-124">FileB. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="0f652-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="0f652-125">Embora os números de sequência de arquivos na tabela de arquivos não precisem ser consecutivos e arquivos extras possam existir no arquivo de gabinete, a sequência relativa de todos os arquivos na tabela de arquivos deve corresponder à ordem no [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="0f652-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="0f652-126">Para corrigir esse erro, altere o número de sequência de FileB para que ele chegue após FileC para corresponder à ordem do arquivo no CAB ou reconstrua o CAB com os arquivos na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="0f652-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f652-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f652-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f652-128">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="0f652-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



