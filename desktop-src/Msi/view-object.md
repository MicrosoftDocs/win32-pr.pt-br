---
description: O objeto View representa um conjunto de resultados obtido ao processar uma consulta usando o método OpenView do objeto Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Exibir objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790030"
---
# <a name="view-object"></a><span data-ttu-id="e1d10-103">Exibir objeto</span><span class="sxs-lookup"><span data-stu-id="e1d10-103">View object</span></span>

<span data-ttu-id="e1d10-104">O objeto **View** representa um conjunto de resultados obtido ao processar uma consulta usando o método [**OpenView**](database-openview.md) do objeto [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d10-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="e1d10-105">Antes que qualquer dado possa ser transferido, a consulta deve ser executada usando o método [**Execute**](view-execute.md) , passando para todos os parâmetros substituíveis designados na cadeia de caracteres de consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="e1d10-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="e1d10-106">A consulta pode ser executada novamente, com parâmetros diferentes, se necessário, mas somente depois de liberar o conjunto de resultados, seja buscando todos os registros ou chamando o método [**Close**](view-close.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d10-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="e1d10-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e1d10-107">Members</span></span>

<span data-ttu-id="e1d10-108">O objeto **View** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e1d10-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="e1d10-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1d10-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1d10-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1d10-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e1d10-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1d10-111">Methods</span></span>

<span data-ttu-id="e1d10-112">O objeto **View** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e1d10-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="e1d10-113">Método</span><span class="sxs-lookup"><span data-stu-id="e1d10-113">Method</span></span>                            | <span data-ttu-id="e1d10-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1d10-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1d10-115">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="e1d10-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="e1d10-116">Encerra a execução da consulta e libera recursos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1d10-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="e1d10-117">**Executados**</span><span class="sxs-lookup"><span data-stu-id="e1d10-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="e1d10-118">Usa o token de ponto de interrogação para representar parâmetros em uma consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="e1d10-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="e1d10-119">Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1d10-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="e1d10-120">**Obtida**</span><span class="sxs-lookup"><span data-stu-id="e1d10-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="e1d10-121">Retorna um objeto [**Record**](record-object.md) contendo os dados de coluna solicitados se mais linhas estiverem disponíveis no conjunto de resultados, caso contrário, retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="e1d10-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="e1d10-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="e1d10-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="e1d10-123">Retorna o erro de validação e o nome da coluna para o qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e1d10-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e1d10-124">**Alterar**</span><span class="sxs-lookup"><span data-stu-id="e1d10-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="e1d10-125">Modifica uma linha de banco de dados com um objeto de [**registro**](record-object.md) modificado obtido pelo método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d10-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="e1d10-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1d10-126">Properties</span></span>

<span data-ttu-id="e1d10-127">O objeto **View** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1d10-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="e1d10-128">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e1d10-128">Property</span></span>                                         | <span data-ttu-id="e1d10-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1d10-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1d10-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="e1d10-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="e1d10-131">Retorna um objeto de [**registro**](record-object.md) que contém as informações solicitadas sobre cada coluna no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e1d10-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e1d10-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d10-132">Requirements</span></span>



| <span data-ttu-id="e1d10-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d10-133">Requirement</span></span> | <span data-ttu-id="e1d10-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d10-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d10-135">Versão</span><span class="sxs-lookup"><span data-stu-id="e1d10-135">Version</span></span><br/> | <span data-ttu-id="e1d10-136">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1d10-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1d10-137">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1d10-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1d10-138">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1d10-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1d10-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e1d10-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1d10-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d10-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1d10-141">IID</span><span class="sxs-lookup"><span data-stu-id="e1d10-141">IID</span></span><br/>     | <span data-ttu-id="e1d10-142">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1d10-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="e1d10-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1d10-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d10-144">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e1d10-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




