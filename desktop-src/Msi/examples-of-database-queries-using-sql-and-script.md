---
description: Um exemplo de uso de consultas de banco de dados controladas por script é fornecido no SDK (Software Development Kit) Windows Installer como o WiRunSQL.vbs do utilitário.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Exemplos de consultas de banco de dados usando SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661913"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="51145-103">Exemplos de consultas de banco de dados usando SQL e script</span><span class="sxs-lookup"><span data-stu-id="51145-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="51145-104">Um exemplo de uso de consultas de banco de dados controladas por script é fornecido no SDK ( [Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) ) do Windows Installer como o utilitário WiRunSQL.vbs.</span><span class="sxs-lookup"><span data-stu-id="51145-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="51145-105">Esse utilitário trata as consultas de banco de dados usando a versão Windows Installer do SQL descrita na sintaxe da seção [SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="51145-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="51145-106">**Excluir um registro de uma tabela**</span><span class="sxs-lookup"><span data-stu-id="51145-106">**Delete a record from a table**</span></span>

<span data-ttu-id="51145-107">A linha de comando a seguir exclui o registro com a chave primária vermelha da tabela de [recursos](feature-table.md) do banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="51145-108">**Cscript WiRunSQL.vbs Test.msi "excluir do \` recurso \` em que o \` recurso \` . \` Recurso \` = ' vermelho ' "**</span><span class="sxs-lookup"><span data-stu-id="51145-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="51145-109">**Adicionar uma tabela a um banco de dados**</span><span class="sxs-lookup"><span data-stu-id="51145-109">**Add a table to a database**</span></span>

<span data-ttu-id="51145-110">A linha de comando a seguir adiciona a tabela de [diretórios](directory-table.md) ao banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="51145-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory \` ( \` diretório \` Char (72) NOT NULL, \` diretório \_ pai \` Char (72), \` DefaultDir \` Char (255) não NULL localizály Primary Key \` Directory \` )"**</span><span class="sxs-lookup"><span data-stu-id="51145-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="51145-112">**Remover uma tabela de um banco de dados**</span><span class="sxs-lookup"><span data-stu-id="51145-112">**Remove a table from a database**</span></span>

<span data-ttu-id="51145-113">A linha de comando a seguir remove a tabela de [recursos](feature-table.md) do banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="51145-114">**Cscript WiRunSQL.vbs Test.msi "recurso de descartar tabela \` \` "**</span><span class="sxs-lookup"><span data-stu-id="51145-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="51145-115">**Adicionar uma nova coluna a uma tabela**</span><span class="sxs-lookup"><span data-stu-id="51145-115">**Add a new column to a table**</span></span>

<span data-ttu-id="51145-116">A linha de comando a seguir adiciona a coluna de teste à tabela [CustomAction](customaction-table.md) do banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="51145-117">**CScript WiRunSQL.vbs Test.msi "alterar tabela \` CustomAction \` Adicionar \` inteiro de teste \` "**</span><span class="sxs-lookup"><span data-stu-id="51145-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="51145-118">**Inserir um novo registro em uma tabela**</span><span class="sxs-lookup"><span data-stu-id="51145-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="51145-119">A linha de comando a seguir insere um novo registro na tabela de [recursos](feature-table.md) do banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="51145-120">**Cscript WiRunSQL.vbs Test.msi "recurso inserir \` em \` ( \` recurso \` . \` Recurso \` , \` recurso \` . \` Recurso \_ pai \` , \` recurso \` . \` Título \` , \` recurso \` . \` Descrição \` , \` recurso \` . \` Exibir \` , \` recurso \` . \` Nível \` , \` recurso \` . \` Diretório \_ \` , \` recurso \` . \` Attributes \` ) valores (' tênis ', ' esporte ', ' tênis ', ' Torneio ', 25, 3, ' SPORTDIR ', 2) "**</span><span class="sxs-lookup"><span data-stu-id="51145-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="51145-121">Isso insere o registro a seguir na tabela de [recursos](feature-table.md) do Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="51145-122">[Recurso](feature-table.md) do Tabela</span><span class="sxs-lookup"><span data-stu-id="51145-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="51145-123">Recurso</span><span class="sxs-lookup"><span data-stu-id="51145-123">Feature</span></span> | <span data-ttu-id="51145-124">Pai do recurso \_</span><span class="sxs-lookup"><span data-stu-id="51145-124">Feature\_Parent</span></span> | <span data-ttu-id="51145-125">Título</span><span class="sxs-lookup"><span data-stu-id="51145-125">Title</span></span>  | <span data-ttu-id="51145-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="51145-126">Description</span></span> | <span data-ttu-id="51145-127">Monitor</span><span class="sxs-lookup"><span data-stu-id="51145-127">Display</span></span> | <span data-ttu-id="51145-128">Nível</span><span class="sxs-lookup"><span data-stu-id="51145-128">Level</span></span> | <span data-ttu-id="51145-129">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="51145-129">Directory\_</span></span> | <span data-ttu-id="51145-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="51145-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="51145-131">Quadra</span><span class="sxs-lookup"><span data-stu-id="51145-131">Tennis</span></span>  | <span data-ttu-id="51145-132">Esporte</span><span class="sxs-lookup"><span data-stu-id="51145-132">Sport</span></span>           | <span data-ttu-id="51145-133">Quadra</span><span class="sxs-lookup"><span data-stu-id="51145-133">Tennis</span></span> | <span data-ttu-id="51145-134">Torneio</span><span class="sxs-lookup"><span data-stu-id="51145-134">Tournament</span></span>  | <span data-ttu-id="51145-135">25</span><span class="sxs-lookup"><span data-stu-id="51145-135">25</span></span>      | <span data-ttu-id="51145-136">3</span><span class="sxs-lookup"><span data-stu-id="51145-136">3</span></span>     | <span data-ttu-id="51145-137">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="51145-137">SPORTDIR</span></span>    | <span data-ttu-id="51145-138">2</span><span class="sxs-lookup"><span data-stu-id="51145-138">2</span></span>          |



 

<span data-ttu-id="51145-139">Observe que os dados binários não podem ser inseridos em uma tabela diretamente usando a inserção ou a atualização de consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="51145-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="51145-140">Para obter informações, consulte [adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="51145-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="51145-141">**Modificar um registro existente em uma tabela**</span><span class="sxs-lookup"><span data-stu-id="51145-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="51145-142">A linha de comando a seguir altera o valor existente no campo título para "desempenho".</span><span class="sxs-lookup"><span data-stu-id="51145-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="51145-143">O registro atualizado tem "Artes" como sua chave primária e está na tabela de recursos do banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="51145-144">**Cscript WiRunSQL.vbs Test.msi recurso " \` Atualizar \` conjunto de recursos \` \` . \` Title \` = ' desempenho ' em que \` recurso \` . \` Recurso \` = ' artes ' "**</span><span class="sxs-lookup"><span data-stu-id="51145-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="51145-145">**Selecionar um grupo de registros**</span><span class="sxs-lookup"><span data-stu-id="51145-145">**Select a group of records**</span></span>

<span data-ttu-id="51145-146">A linha de comando a seguir seleciona o nome e o tipo de todos os controles que pertencem ao ErrorDialog no banco de dados Test.msi.</span><span class="sxs-lookup"><span data-stu-id="51145-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="51145-147">**CScript WiRunSQL.vbs Test.msi "selecionar \` controle \` , \` tipo \` de \` controle \` onde \` caixa de diálogo \_ \` = ' ErrorDialog '"**</span><span class="sxs-lookup"><span data-stu-id="51145-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="51145-148">**Manter uma tabela na memória**</span><span class="sxs-lookup"><span data-stu-id="51145-148">**Hold a table in memory**</span></span>

<span data-ttu-id="51145-149">A linha de comando a seguir bloqueia a tabela de [componentes](component-table.md) do banco de dados Test.msi na memória.</span><span class="sxs-lookup"><span data-stu-id="51145-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="51145-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` componente \` Hold"**</span><span class="sxs-lookup"><span data-stu-id="51145-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="51145-151">**Liberar uma tabela na memória**</span><span class="sxs-lookup"><span data-stu-id="51145-151">**Free a table in memory**</span></span>

<span data-ttu-id="51145-152">A linha de comando a seguir libera a tabela de [componentes](component-table.md) do banco de dados Test.msi da memória.</span><span class="sxs-lookup"><span data-stu-id="51145-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="51145-153">**CScript WiRunSQL.vbs Test.msi "alterar o \` componente de tabela \` gratuito"**</span><span class="sxs-lookup"><span data-stu-id="51145-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



