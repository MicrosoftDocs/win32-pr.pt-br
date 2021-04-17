---
description: O objeto de banco de dados acessa um banco de dados do instalador.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objeto de banco de dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769323"
---
# <a name="database-object"></a><span data-ttu-id="c1c40-103">Objeto de banco de dados</span><span class="sxs-lookup"><span data-stu-id="c1c40-103">Database object</span></span>

<span data-ttu-id="c1c40-104">O objeto de **banco de dados** acessa um banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="c1c40-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="c1c40-105">O objeto de **banco de dados** é liberado quando ele é retirado do escopo ou quando a variável de objeto associada a ele é definida como NULL.</span><span class="sxs-lookup"><span data-stu-id="c1c40-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="c1c40-106">O método [**Commit**](database-commit.md) deve ser chamado antes que o objeto de **banco de dados** seja liberado para gravar todas as alterações persistentes.</span><span class="sxs-lookup"><span data-stu-id="c1c40-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="c1c40-107">Se o método **Commit** não for chamado, o instalador executará uma reversão implícita após a destruição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c1c40-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="c1c40-108">O cliente pode usar o procedimento a seguir para acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="c1c40-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="c1c40-109">**Para consultar o sequenciamento de API**</span><span class="sxs-lookup"><span data-stu-id="c1c40-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="c1c40-110">Obtenha um objeto de **banco de dados** chamando o objeto [**OpenDatabase**](installer-opendatabase.md) ou [**instalador**](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c40-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="c1c40-111">Inicie uma consulta usando uma cadeia de caracteres SQL chamando o método [**OpenView**](database-openview.md) do objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="c1c40-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="c1c40-112">Defina os parâmetros de consulta em um objeto de [**registro**](record-object.md) e execute a consulta de banco de dados chamando o método [**Execute**](view-execute.md) do objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c40-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="c1c40-113">Isso produz um resultado que pode ser buscado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="c1c40-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="c1c40-114">Chame o método [**Fetch**](view-fetch.md) do objeto [**View**](view-object.md) repetidamente para retornar objetos [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c40-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="c1c40-115">Atualize as linhas de banco de dados de um objeto de [**registro**](record-object.md) obtido pelo método [**Fetch**](view-fetch.md) usando o método [**Modify**](view-modify.md) do objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c40-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="c1c40-116">Libere a consulta e todos os registros não buscados chamando o método [**Close**](view-close.md) do objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c40-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="c1c40-117">Mantenha todas as atualizações de banco de dados chamando o método [**Commit**](database-commit.md) do objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="c1c40-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="c1c40-118">Membros</span><span class="sxs-lookup"><span data-stu-id="c1c40-118">Members</span></span>

<span data-ttu-id="c1c40-119">O objeto de **banco de dados** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1c40-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="c1c40-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1c40-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1c40-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1c40-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1c40-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1c40-122">Methods</span></span>

<span data-ttu-id="c1c40-123">O objeto de **banco de dados** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1c40-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="c1c40-124">Método</span><span class="sxs-lookup"><span data-stu-id="c1c40-124">Method</span></span>                                                                    | <span data-ttu-id="c1c40-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1c40-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1c40-126">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="c1c40-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="c1c40-127">Aplica a transformação a este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1c40-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c1c40-128">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="c1c40-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="c1c40-129">Finaliza a forma persistente do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1c40-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="c1c40-130">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="c1c40-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="c1c40-131">Cria e popula o fluxo de informações resumidas de um arquivo de transformação existente.</span><span class="sxs-lookup"><span data-stu-id="c1c40-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="c1c40-132">**EnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="c1c40-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="c1c40-133">Facilita a criação de caixas de diálogo e de mural, fornecendo o suporte necessário para exibir caixas de diálogo da interface do usuário armazenadas no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="c1c40-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="c1c40-134">**Exportação**</span><span class="sxs-lookup"><span data-stu-id="c1c40-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="c1c40-135">Copia a estrutura e os dados de uma tabela especificada para um arquivo morto de texto.</span><span class="sxs-lookup"><span data-stu-id="c1c40-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c1c40-136">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="c1c40-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="c1c40-137">Cria uma transformação.</span><span class="sxs-lookup"><span data-stu-id="c1c40-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="c1c40-138">**Importar**</span><span class="sxs-lookup"><span data-stu-id="c1c40-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="c1c40-139">Importa uma tabela de banco de dados de um arquivo morto de texto.</span><span class="sxs-lookup"><span data-stu-id="c1c40-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c1c40-140">**Mescle**</span><span class="sxs-lookup"><span data-stu-id="c1c40-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="c1c40-141">Mescla o banco de dados de referência com o banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="c1c40-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="c1c40-142">**AbrirModoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="c1c40-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="c1c40-143">Retorna um objeto [**View**](view-object.md) que representa a consulta especificada por uma cadeia de caracteres SQL.</span><span class="sxs-lookup"><span data-stu-id="c1c40-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="c1c40-144">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1c40-144">Properties</span></span>

<span data-ttu-id="c1c40-145">O objeto de **banco de dados** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1c40-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="c1c40-146">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c1c40-146">Property</span></span>                                                                               | <span data-ttu-id="c1c40-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1c40-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1c40-148">**Banco de dados**</span><span class="sxs-lookup"><span data-stu-id="c1c40-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="c1c40-149">Retorna o estado de persistência do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1c40-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c1c40-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="c1c40-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="c1c40-151">Retorna um objeto de [**registro**](record-object.md) que contém o nome da tabela e os nomes de coluna (que abrangem as chaves primárias).</span><span class="sxs-lookup"><span data-stu-id="c1c40-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="c1c40-152">**SummaryInformation (objeto de banco de dados)**</span><span class="sxs-lookup"><span data-stu-id="c1c40-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="c1c40-153">Retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="c1c40-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="c1c40-154">**TablePersistent**</span><span class="sxs-lookup"><span data-stu-id="c1c40-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="c1c40-155">Retorna o estado de persistência da tabela.</span><span class="sxs-lookup"><span data-stu-id="c1c40-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="c1c40-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c40-156">Requirements</span></span>



| <span data-ttu-id="c1c40-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c40-157">Requirement</span></span> | <span data-ttu-id="c1c40-158">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c40-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c40-159">Versão</span><span class="sxs-lookup"><span data-stu-id="c1c40-159">Version</span></span><br/> | <span data-ttu-id="c1c40-160">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1c40-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1c40-161">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1c40-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1c40-162">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1c40-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c1c40-163">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c40-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1c40-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c40-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c1c40-165">IID</span><span class="sxs-lookup"><span data-stu-id="c1c40-165">IID</span></span><br/>     | <span data-ttu-id="c1c40-166">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c1c40-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="c1c40-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c40-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c40-168">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c1c40-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




