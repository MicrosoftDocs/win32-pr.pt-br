---
description: A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabela ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501565"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="f2843-103">Tabela ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="f2843-103">ODBCDriver Table</span></span>

<span data-ttu-id="f2843-104">A tabela ODBCDriver lista os drivers ODBC que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="f2843-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="f2843-105">A tabela ODBCDriver tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2843-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="f2843-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="f2843-106">Column</span></span>      | <span data-ttu-id="f2843-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2843-107">Type</span></span>                         | <span data-ttu-id="f2843-108">Chave</span><span class="sxs-lookup"><span data-stu-id="f2843-108">Key</span></span> | <span data-ttu-id="f2843-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f2843-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="f2843-110">Driver</span><span class="sxs-lookup"><span data-stu-id="f2843-110">Driver</span></span>      | [<span data-ttu-id="f2843-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="f2843-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2843-112">S</span><span class="sxs-lookup"><span data-stu-id="f2843-112">Y</span></span>   | <span data-ttu-id="f2843-113">N</span><span class="sxs-lookup"><span data-stu-id="f2843-113">N</span></span>        |
| <span data-ttu-id="f2843-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f2843-114">Component\_</span></span> | [<span data-ttu-id="f2843-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="f2843-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2843-116">N</span><span class="sxs-lookup"><span data-stu-id="f2843-116">N</span></span>   | <span data-ttu-id="f2843-117">N</span><span class="sxs-lookup"><span data-stu-id="f2843-117">N</span></span>        |
| <span data-ttu-id="f2843-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2843-118">Description</span></span> | [<span data-ttu-id="f2843-119">Text</span><span class="sxs-lookup"><span data-stu-id="f2843-119">Text</span></span>](text.md)             | <span data-ttu-id="f2843-120">N</span><span class="sxs-lookup"><span data-stu-id="f2843-120">N</span></span>   | <span data-ttu-id="f2843-121">N</span><span class="sxs-lookup"><span data-stu-id="f2843-121">N</span></span>        |
| <span data-ttu-id="f2843-122">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="f2843-122">File\_</span></span>      | [<span data-ttu-id="f2843-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="f2843-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2843-124">N</span><span class="sxs-lookup"><span data-stu-id="f2843-124">N</span></span>   | <span data-ttu-id="f2843-125">N</span><span class="sxs-lookup"><span data-stu-id="f2843-125">N</span></span>        |
| <span data-ttu-id="f2843-126">Configuração de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f2843-126">File\_Setup</span></span> | [<span data-ttu-id="f2843-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="f2843-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2843-128">N</span><span class="sxs-lookup"><span data-stu-id="f2843-128">N</span></span>   | <span data-ttu-id="f2843-129">S</span><span class="sxs-lookup"><span data-stu-id="f2843-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f2843-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="f2843-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f2843-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span><span class="sxs-lookup"><span data-stu-id="f2843-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="f2843-132">Nome do token interno para o driver.</span><span class="sxs-lookup"><span data-stu-id="f2843-132">Internal token name for driver.</span></span> <span data-ttu-id="f2843-133">Uma chave primária para a tabela</span><span class="sxs-lookup"><span data-stu-id="f2843-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="f2843-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="f2843-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f2843-135">Chave externa na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="f2843-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="f2843-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="f2843-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="f2843-137">A descrição registrada para este driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="f2843-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="f2843-138">Este valor não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="f2843-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="f2843-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="f2843-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f2843-140">O arquivo DLL para os drivers listados na coluna driver.</span><span class="sxs-lookup"><span data-stu-id="f2843-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="f2843-141">A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2843-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="f2843-142">O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="f2843-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="f2843-143">A \| sintaxe SFN LFN não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="f2843-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="f2843-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuração de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f2843-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="f2843-145">O arquivo DLL de instalação para o driver se ele for diferente do driver.</span><span class="sxs-lookup"><span data-stu-id="f2843-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="f2843-146">A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2843-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="f2843-147">O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="f2843-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="f2843-148">A \| sintaxe SFN LFN não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="f2843-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2843-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2843-149">Remarks</span></span>

<span data-ttu-id="f2843-150">As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="f2843-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f2843-151">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2843-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f2843-152">Validação</span><span class="sxs-lookup"><span data-stu-id="f2843-152">Validation</span></span>

<dl>

[<span data-ttu-id="f2843-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="f2843-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f2843-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="f2843-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f2843-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="f2843-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



