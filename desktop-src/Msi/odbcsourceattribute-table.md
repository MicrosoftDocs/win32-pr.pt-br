---
description: A tabela ODBCSourceAttribute contém informações sobre os atributos de fontes de dados.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabela ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501562"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="cb640-103">Tabela ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="cb640-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="cb640-104">A tabela ODBCSourceAttribute contém informações sobre os atributos de fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="cb640-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="cb640-105">A tabela ODBCSourceAttribute tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb640-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="cb640-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="cb640-106">Column</span></span>       | <span data-ttu-id="cb640-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb640-107">Type</span></span>                         | <span data-ttu-id="cb640-108">Chave</span><span class="sxs-lookup"><span data-stu-id="cb640-108">Key</span></span> | <span data-ttu-id="cb640-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb640-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="cb640-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="cb640-110">DataSource\_</span></span> | [<span data-ttu-id="cb640-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="cb640-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="cb640-112">S</span><span class="sxs-lookup"><span data-stu-id="cb640-112">Y</span></span>   | <span data-ttu-id="cb640-113">N</span><span class="sxs-lookup"><span data-stu-id="cb640-113">N</span></span>        |
| <span data-ttu-id="cb640-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="cb640-114">Attribute</span></span>    | [<span data-ttu-id="cb640-115">Text</span><span class="sxs-lookup"><span data-stu-id="cb640-115">Text</span></span>](text.md)             | <span data-ttu-id="cb640-116">S</span><span class="sxs-lookup"><span data-stu-id="cb640-116">Y</span></span>   | <span data-ttu-id="cb640-117">N</span><span class="sxs-lookup"><span data-stu-id="cb640-117">N</span></span>        |
| <span data-ttu-id="cb640-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cb640-118">Value</span></span>        | [<span data-ttu-id="cb640-119">Binário</span><span class="sxs-lookup"><span data-stu-id="cb640-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="cb640-120">N</span><span class="sxs-lookup"><span data-stu-id="cb640-120">N</span></span>   | <span data-ttu-id="cb640-121">S</span><span class="sxs-lookup"><span data-stu-id="cb640-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb640-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="cb640-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb640-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Fonte\_</span><span class="sxs-lookup"><span data-stu-id="cb640-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="cb640-124">Nome do token interno para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="cb640-124">Internal token name for data source.</span></span> <span data-ttu-id="cb640-125">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="cb640-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="cb640-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="cb640-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="cb640-127">Nome do atributo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="cb640-127">Name of data source attribute.</span></span> <span data-ttu-id="cb640-128">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="cb640-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="cb640-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="cb640-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="cb640-130">O valor de cadeia de caracteres localizável para o atributo.</span><span class="sxs-lookup"><span data-stu-id="cb640-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb640-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb640-131">Remarks</span></span>

<span data-ttu-id="cb640-132">As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="cb640-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="cb640-133">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb640-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="cb640-134">Validação</span><span class="sxs-lookup"><span data-stu-id="cb640-134">Validation</span></span>

<dl>

[<span data-ttu-id="cb640-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="cb640-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cb640-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="cb640-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cb640-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="cb640-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="cb640-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="cb640-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



