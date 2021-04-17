---
description: A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabela ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754349"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="7d692-103">Tabela ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="7d692-103">ODBCDataSource Table</span></span>

<span data-ttu-id="7d692-104">A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="7d692-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="7d692-105">A tabela ODBCDataSource tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d692-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="7d692-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="7d692-106">Column</span></span>            | <span data-ttu-id="7d692-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d692-107">Type</span></span>                         | <span data-ttu-id="7d692-108">Chave</span><span class="sxs-lookup"><span data-stu-id="7d692-108">Key</span></span> | <span data-ttu-id="7d692-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7d692-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="7d692-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="7d692-110">DataSource</span></span>        | [<span data-ttu-id="7d692-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="7d692-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="7d692-112">S</span><span class="sxs-lookup"><span data-stu-id="7d692-112">Y</span></span>   | <span data-ttu-id="7d692-113">N</span><span class="sxs-lookup"><span data-stu-id="7d692-113">N</span></span>        |
| <span data-ttu-id="7d692-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7d692-114">Component\_</span></span>       | [<span data-ttu-id="7d692-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="7d692-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="7d692-116">N</span><span class="sxs-lookup"><span data-stu-id="7d692-116">N</span></span>   | <span data-ttu-id="7d692-117">N</span><span class="sxs-lookup"><span data-stu-id="7d692-117">N</span></span>        |
| <span data-ttu-id="7d692-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d692-118">Description</span></span>       | [<span data-ttu-id="7d692-119">Text</span><span class="sxs-lookup"><span data-stu-id="7d692-119">Text</span></span>](text.md)             | <span data-ttu-id="7d692-120">N</span><span class="sxs-lookup"><span data-stu-id="7d692-120">N</span></span>   | <span data-ttu-id="7d692-121">N</span><span class="sxs-lookup"><span data-stu-id="7d692-121">N</span></span>        |
| <span data-ttu-id="7d692-122">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="7d692-122">DriverDescription</span></span> | [<span data-ttu-id="7d692-123">Text</span><span class="sxs-lookup"><span data-stu-id="7d692-123">Text</span></span>](text.md)             | <span data-ttu-id="7d692-124">N</span><span class="sxs-lookup"><span data-stu-id="7d692-124">N</span></span>   | <span data-ttu-id="7d692-125">N</span><span class="sxs-lookup"><span data-stu-id="7d692-125">N</span></span>        |
| <span data-ttu-id="7d692-126">Registro</span><span class="sxs-lookup"><span data-stu-id="7d692-126">Registration</span></span>      | [<span data-ttu-id="7d692-127">Inteiro</span><span class="sxs-lookup"><span data-stu-id="7d692-127">Integer</span></span>](integer.md)       | <span data-ttu-id="7d692-128">N</span><span class="sxs-lookup"><span data-stu-id="7d692-128">N</span></span>   | <span data-ttu-id="7d692-129">N</span><span class="sxs-lookup"><span data-stu-id="7d692-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7d692-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="7d692-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7d692-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Fonte</span><span class="sxs-lookup"><span data-stu-id="7d692-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="7d692-132">Nome do token interno para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7d692-132">Internal token name for data source.</span></span> <span data-ttu-id="7d692-133">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="7d692-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="7d692-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="7d692-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="7d692-135">Chave externa na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d692-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d692-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="7d692-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="7d692-137">A descrição registrada para esta fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7d692-137">The description registered for this data source.</span></span> <span data-ttu-id="7d692-138">Este valor não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="7d692-138">This value cannot be localized.</span></span> <span data-ttu-id="7d692-139">As descrições da fonte de dados ODBC não podem exceder o \_ comprimento máximo do DSN do SQL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7d692-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="7d692-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span><span class="sxs-lookup"><span data-stu-id="7d692-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="7d692-141">Driver associado que pode ser preexistente.</span><span class="sxs-lookup"><span data-stu-id="7d692-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="7d692-142">Este valor não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="7d692-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="7d692-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Falta</span><span class="sxs-lookup"><span data-stu-id="7d692-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="7d692-144">Este campo especifica o tipo de registro para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7d692-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="7d692-145">Constante</span><span class="sxs-lookup"><span data-stu-id="7d692-145">Constant</span></span>                                      | <span data-ttu-id="7d692-146">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7d692-146">Hexadecimal</span></span> | <span data-ttu-id="7d692-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="7d692-147">Decimal</span></span> | <span data-ttu-id="7d692-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d692-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="7d692-149">**msidbODBCDataSourceRegistrationPerMachine**</span><span class="sxs-lookup"><span data-stu-id="7d692-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="7d692-150">0x000</span><span class="sxs-lookup"><span data-stu-id="7d692-150">0x000</span></span>       | <span data-ttu-id="7d692-151">0</span><span class="sxs-lookup"><span data-stu-id="7d692-151">0</span></span>       | <span data-ttu-id="7d692-152">A fonte de dados é registrada por computador.</span><span class="sxs-lookup"><span data-stu-id="7d692-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="7d692-153">**msidbODBCDataSourceRegistrationPerUser**</span><span class="sxs-lookup"><span data-stu-id="7d692-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="7d692-154">0x001</span><span class="sxs-lookup"><span data-stu-id="7d692-154">0x001</span></span>       | <span data-ttu-id="7d692-155">1</span><span class="sxs-lookup"><span data-stu-id="7d692-155">1</span></span>       | <span data-ttu-id="7d692-156">A fonte de dados é registrada por usuário.</span><span class="sxs-lookup"><span data-stu-id="7d692-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d692-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d692-157">Remarks</span></span>

<span data-ttu-id="7d692-158">As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="7d692-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="7d692-159">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d692-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7d692-160">Validação</span><span class="sxs-lookup"><span data-stu-id="7d692-160">Validation</span></span>

<dl>

[<span data-ttu-id="7d692-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="7d692-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7d692-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="7d692-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7d692-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="7d692-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7d692-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="7d692-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="7d692-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="7d692-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



