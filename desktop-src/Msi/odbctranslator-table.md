---
description: A tabela ODBCTranslator lista os conversores ODBC que pertencem à instalação.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabela ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751644"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="5f20e-103">Tabela ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="5f20e-103">ODBCTranslator Table</span></span>

<span data-ttu-id="5f20e-104">A tabela ODBCTranslator lista os conversores ODBC que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="5f20e-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="5f20e-105">A tabela ODBCTranslator tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f20e-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="5f20e-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="5f20e-106">Column</span></span>      | <span data-ttu-id="5f20e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f20e-107">Type</span></span>                         | <span data-ttu-id="5f20e-108">Chave</span><span class="sxs-lookup"><span data-stu-id="5f20e-108">Key</span></span> | <span data-ttu-id="5f20e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="5f20e-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="5f20e-110">Tradutor</span><span class="sxs-lookup"><span data-stu-id="5f20e-110">Translator</span></span>  | [<span data-ttu-id="5f20e-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="5f20e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="5f20e-112">S</span><span class="sxs-lookup"><span data-stu-id="5f20e-112">Y</span></span>   | <span data-ttu-id="5f20e-113">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-113">N</span></span>        |
| <span data-ttu-id="5f20e-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5f20e-114">Component\_</span></span> | [<span data-ttu-id="5f20e-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="5f20e-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="5f20e-116">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-116">N</span></span>   | <span data-ttu-id="5f20e-117">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-117">N</span></span>        |
| <span data-ttu-id="5f20e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f20e-118">Description</span></span> | [<span data-ttu-id="5f20e-119">Text</span><span class="sxs-lookup"><span data-stu-id="5f20e-119">Text</span></span>](text.md)             | <span data-ttu-id="5f20e-120">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-120">N</span></span>   | <span data-ttu-id="5f20e-121">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-121">N</span></span>        |
| <span data-ttu-id="5f20e-122">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="5f20e-122">File\_</span></span>      | [<span data-ttu-id="5f20e-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="5f20e-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="5f20e-124">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-124">N</span></span>   | <span data-ttu-id="5f20e-125">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-125">N</span></span>        |
| <span data-ttu-id="5f20e-126">Configuração de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="5f20e-126">File\_Setup</span></span> | [<span data-ttu-id="5f20e-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="5f20e-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="5f20e-128">N</span><span class="sxs-lookup"><span data-stu-id="5f20e-128">N</span></span>   | <span data-ttu-id="5f20e-129">S</span><span class="sxs-lookup"><span data-stu-id="5f20e-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5f20e-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="5f20e-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5f20e-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="5f20e-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="5f20e-132">Nome do token interno para o tradutor.</span><span class="sxs-lookup"><span data-stu-id="5f20e-132">Internal token name for translator.</span></span> <span data-ttu-id="5f20e-133">Uma chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="5f20e-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="5f20e-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="5f20e-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="5f20e-135">Chave externa na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="5f20e-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="5f20e-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="5f20e-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="5f20e-137">A descrição registrada para este conversor de driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="5f20e-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="5f20e-138">Este valor não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="5f20e-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="5f20e-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="5f20e-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="5f20e-140">O arquivo DLL para a transferência listada na coluna tradutor.</span><span class="sxs-lookup"><span data-stu-id="5f20e-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="5f20e-141">A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="5f20e-142">O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="5f20e-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="5f20e-143">A \| sintaxe SFN LFN não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="5f20e-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="5f20e-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuração de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="5f20e-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="5f20e-145">O arquivo DLL de instalação para o tradutor se ele for diferente da coluna tradutor.</span><span class="sxs-lookup"><span data-stu-id="5f20e-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="5f20e-146">A \_ coluna File é uma chave externa na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="5f20e-147">O nome de arquivo inserido na coluna filename desse registro de tabela de arquivos deve estar no formato de nome de arquivo curto.</span><span class="sxs-lookup"><span data-stu-id="5f20e-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="5f20e-148">A \| sintaxe SFN LFN não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="5f20e-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f20e-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f20e-149">Remarks</span></span>

<span data-ttu-id="5f20e-150">As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="5f20e-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="5f20e-151">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="5f20e-152">Validação</span><span class="sxs-lookup"><span data-stu-id="5f20e-152">Validation</span></span>

<dl>

[<span data-ttu-id="5f20e-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="5f20e-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5f20e-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="5f20e-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5f20e-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="5f20e-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



