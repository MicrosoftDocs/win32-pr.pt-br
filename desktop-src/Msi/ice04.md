---
description: ICE04 valida que o número de sequência de cada arquivo na tabela de arquivos é menor ou igual ao maior número de sequência na coluna LastSequence da tabela de mídia.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922026"
---
# <a name="ice04"></a><span data-ttu-id="47611-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="47611-103">ICE04</span></span>

<span data-ttu-id="47611-104">ICE04 valida que o número de sequência de cada arquivo na [tabela de arquivos](file-table.md) é menor ou igual ao maior número de sequência na coluna LastSequence da [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="47611-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="47611-105">Cada registro na tabela de mídia representa um disco na mídia de origem que contém todos os arquivos com um número de sequência menor ou igual ao valor na coluna LastSequence e maior que o valor de LastSequence no registro do disco anterior.</span><span class="sxs-lookup"><span data-stu-id="47611-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="47611-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="47611-106">Result</span></span>

<span data-ttu-id="47611-107">ICE04 posta uma mensagem de erro se houver um arquivo com um número de sequência maior que o maior número de LastSequence para a mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="47611-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="47611-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47611-108">Example</span></span>

<span data-ttu-id="47611-109">ICE04 relataria o seguinte erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="47611-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="47611-110">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="47611-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="47611-111">Arquivo</span><span class="sxs-lookup"><span data-stu-id="47611-111">File</span></span>   | <span data-ttu-id="47611-112">Sequência</span><span class="sxs-lookup"><span data-stu-id="47611-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="47611-113">MyFile</span><span class="sxs-lookup"><span data-stu-id="47611-113">MyFile</span></span> | <span data-ttu-id="47611-114">210</span><span class="sxs-lookup"><span data-stu-id="47611-114">210</span></span>      |



 

<span data-ttu-id="47611-115">[Tabela de mídia](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="47611-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="47611-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="47611-116">DiskId</span></span> | <span data-ttu-id="47611-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="47611-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="47611-118">1</span><span class="sxs-lookup"><span data-stu-id="47611-118">1</span></span>      | <span data-ttu-id="47611-119">100</span><span class="sxs-lookup"><span data-stu-id="47611-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="47611-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47611-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47611-121">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="47611-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



