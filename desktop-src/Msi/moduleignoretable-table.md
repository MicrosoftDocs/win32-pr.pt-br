---
description: Se uma tabela no módulo de mesclagem estiver listada na tabela ModuleIgnoreTable, ela não será mesclada no arquivo. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabela ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171492"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="f3114-103">Tabela ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="f3114-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="f3114-104">Se uma tabela no módulo de mesclagem estiver listada na tabela ModuleIgnoreTable, ela não será mesclada no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="f3114-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="f3114-105">Se a tabela já existir no arquivo. msi, ela não será modificada pela mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f3114-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="f3114-106">As tabelas no ModuleIgnoreTable podem, portanto, conter dados desnecessários após a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f3114-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="f3114-107">A tabela ModuleIgnoreTable tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3114-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="f3114-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="f3114-108">Column</span></span> | <span data-ttu-id="f3114-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3114-109">Type</span></span>                         | <span data-ttu-id="f3114-110">Chave</span><span class="sxs-lookup"><span data-stu-id="f3114-110">Key</span></span> | <span data-ttu-id="f3114-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f3114-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="f3114-112">Tabela</span><span class="sxs-lookup"><span data-stu-id="f3114-112">Table</span></span>  | [<span data-ttu-id="f3114-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="f3114-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="f3114-114">S</span><span class="sxs-lookup"><span data-stu-id="f3114-114">Y</span></span>   | <span data-ttu-id="f3114-115">Não</span><span class="sxs-lookup"><span data-stu-id="f3114-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="f3114-116">Colunas</span><span class="sxs-lookup"><span data-stu-id="f3114-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f3114-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="f3114-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="f3114-118">Nome da tabela no módulo de mesclagem que não deve ser mesclado no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="f3114-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3114-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3114-119">Remarks</span></span>

<span data-ttu-id="f3114-120">Para minimizar o tamanho do arquivo. msm, é recomendável que os desenvolvedores removam tabelas não utilizadas de módulos destinados a redistribuição, em vez de listar essas tabelas na tabela ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="f3114-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



