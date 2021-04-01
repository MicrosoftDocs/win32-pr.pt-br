---
description: A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabela ODBCattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090939"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="7bfd2-103">Tabela ODBCattribute</span><span class="sxs-lookup"><span data-stu-id="7bfd2-103">ODBCAttribute Table</span></span>

<span data-ttu-id="7bfd2-104">A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="7bfd2-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="7bfd2-105">A tabela ODBCattribute tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="7bfd2-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="7bfd2-106">Column</span></span>    | <span data-ttu-id="7bfd2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bfd2-107">Type</span></span>                         | <span data-ttu-id="7bfd2-108">Chave</span><span class="sxs-lookup"><span data-stu-id="7bfd2-108">Key</span></span> | <span data-ttu-id="7bfd2-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7bfd2-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="7bfd2-110">Driver\_</span><span class="sxs-lookup"><span data-stu-id="7bfd2-110">Driver\_</span></span>  | [<span data-ttu-id="7bfd2-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="7bfd2-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="7bfd2-112">S</span><span class="sxs-lookup"><span data-stu-id="7bfd2-112">Y</span></span>   | <span data-ttu-id="7bfd2-113">N</span><span class="sxs-lookup"><span data-stu-id="7bfd2-113">N</span></span>        |
| <span data-ttu-id="7bfd2-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="7bfd2-114">Attribute</span></span> | [<span data-ttu-id="7bfd2-115">Text</span><span class="sxs-lookup"><span data-stu-id="7bfd2-115">Text</span></span>](text.md)             | <span data-ttu-id="7bfd2-116">S</span><span class="sxs-lookup"><span data-stu-id="7bfd2-116">Y</span></span>   | <span data-ttu-id="7bfd2-117">N</span><span class="sxs-lookup"><span data-stu-id="7bfd2-117">N</span></span>        |
| <span data-ttu-id="7bfd2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7bfd2-118">Value</span></span>     | [<span data-ttu-id="7bfd2-119">Binário</span><span class="sxs-lookup"><span data-stu-id="7bfd2-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="7bfd2-120">N</span><span class="sxs-lookup"><span data-stu-id="7bfd2-120">N</span></span>   | <span data-ttu-id="7bfd2-121">S</span><span class="sxs-lookup"><span data-stu-id="7bfd2-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7bfd2-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="7bfd2-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7bfd2-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span><span class="sxs-lookup"><span data-stu-id="7bfd2-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="7bfd2-124">Nome de token interno para um driver.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-124">Internal token name for a driver.</span></span> <span data-ttu-id="7bfd2-125">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-125">A primary key for the table.</span></span> <span data-ttu-id="7bfd2-126">Uma chave estrangeira na [tabela ODBCDriver](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="7bfd2-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bfd2-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="7bfd2-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="7bfd2-128">Nome do atributo do driver.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-128">Name of the driver attribute.</span></span> <span data-ttu-id="7bfd2-129">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="7bfd2-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="7bfd2-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="7bfd2-131">Valor de cadeia de caracteres localizável para o atributo.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bfd2-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bfd2-132">Remarks</span></span>

<span data-ttu-id="7bfd2-133">As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="7bfd2-134">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7bfd2-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7bfd2-135">Validação</span><span class="sxs-lookup"><span data-stu-id="7bfd2-135">Validation</span></span>

<dl>

[<span data-ttu-id="7bfd2-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="7bfd2-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7bfd2-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="7bfd2-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7bfd2-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="7bfd2-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7bfd2-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="7bfd2-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



