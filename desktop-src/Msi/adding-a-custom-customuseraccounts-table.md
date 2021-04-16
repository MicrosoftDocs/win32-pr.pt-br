---
description: Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não embutidas em código na ação personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Adicionando uma tabela CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750258"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="1b61b-103">Adicionando uma tabela CustomUserAccounts personalizada</span><span class="sxs-lookup"><span data-stu-id="1b61b-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="1b61b-104">Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não embutidas em código na ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="1b61b-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="1b61b-105">Adicione uma tabela personalizada ao banco de dados de instalação de exemplo chamado CustomUserAccounts para manter as informações da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="1b61b-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="1b61b-106">Consulte [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md) para obter um exemplo de como adicionar uma tabela personalizada.</span><span class="sxs-lookup"><span data-stu-id="1b61b-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="1b61b-107">Use o esquema a seguir para a tabela CustomUserAccounts.</span><span class="sxs-lookup"><span data-stu-id="1b61b-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="1b61b-108">Consulte [formato de definição de coluna](column-definition-format.md) para obter uma explicação dos tipos de coluna.</span><span class="sxs-lookup"><span data-stu-id="1b61b-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="1b61b-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="1b61b-109">Column</span></span>     | <span data-ttu-id="1b61b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b61b-110">Type</span></span> | <span data-ttu-id="1b61b-111">Chave</span><span class="sxs-lookup"><span data-stu-id="1b61b-111">Key</span></span> | <span data-ttu-id="1b61b-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="1b61b-112">Nullable</span></span> | <span data-ttu-id="1b61b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b61b-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b61b-114">UserName</span><span class="sxs-lookup"><span data-stu-id="1b61b-114">UserName</span></span>   | <span data-ttu-id="1b61b-115">s72</span><span class="sxs-lookup"><span data-stu-id="1b61b-115">s72</span></span>  | <span data-ttu-id="1b61b-116">S</span><span class="sxs-lookup"><span data-stu-id="1b61b-116">Y</span></span>   | <span data-ttu-id="1b61b-117">N</span><span class="sxs-lookup"><span data-stu-id="1b61b-117">N</span></span>        | <span data-ttu-id="1b61b-118">Nome da conta de usuário que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="1b61b-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b61b-119">Senha</span><span class="sxs-lookup"><span data-stu-id="1b61b-119">Password</span></span>   | <span data-ttu-id="1b61b-120">s72</span><span class="sxs-lookup"><span data-stu-id="1b61b-120">s72</span></span>  |     | <span data-ttu-id="1b61b-121">N</span><span class="sxs-lookup"><span data-stu-id="1b61b-121">N</span></span>        | <span data-ttu-id="1b61b-122">Nome da propriedade que contém a senha da conta.</span><span class="sxs-lookup"><span data-stu-id="1b61b-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="1b61b-123">Essa é uma [propriedade pública](public-properties.md) definida na linha de comando ou por meio de um [controle de edição](edit-control.md) na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1b61b-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="1b61b-124">Esse controle de edição deve ter o [atributo de controle de senha](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="1b61b-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="1b61b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b61b-125">Attributes</span></span> | <span data-ttu-id="1b61b-126">i4</span><span class="sxs-lookup"><span data-stu-id="1b61b-126">i4</span></span>   |     | <span data-ttu-id="1b61b-127">S</span><span class="sxs-lookup"><span data-stu-id="1b61b-127">Y</span></span>        | <span data-ttu-id="1b61b-128">Atributos para a conta.</span><span class="sxs-lookup"><span data-stu-id="1b61b-128">Attributes for account.</span></span> <span data-ttu-id="1b61b-129">Eles são definidos como os valores **DWORD** para o \_ membro flags usri1 da estrutura info do usuário \_ \_ 1.</span><span class="sxs-lookup"><span data-stu-id="1b61b-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="1b61b-130">Depois que a tabela CustomUserAccounts tiver sido adicionada ao banco de dados, você poderá editar essa tabela usando orca, um editor de tabela fornecido com o SDK do Windows Installer ou outro editor.</span><span class="sxs-lookup"><span data-stu-id="1b61b-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="1b61b-131">Insira o registro a seguir na tabela CustomUserAccounts para criar uma conta de usuário protegida por senha para um usuário chamado TestUser.</span><span class="sxs-lookup"><span data-stu-id="1b61b-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="1b61b-132">Observe que 512 é o valor numérico para a \_ conta normal da UF \_ .</span><span class="sxs-lookup"><span data-stu-id="1b61b-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="1b61b-133">Tabela CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="1b61b-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="1b61b-134">UserName</span><span class="sxs-lookup"><span data-stu-id="1b61b-134">UserName</span></span> | <span data-ttu-id="1b61b-135">Senha</span><span class="sxs-lookup"><span data-stu-id="1b61b-135">Password</span></span>         | <span data-ttu-id="1b61b-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b61b-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="1b61b-137">User</span><span class="sxs-lookup"><span data-stu-id="1b61b-137">TestUser</span></span> | <span data-ttu-id="1b61b-138">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="1b61b-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="1b61b-139">512</span><span class="sxs-lookup"><span data-stu-id="1b61b-139">512</span></span>        |



 

<span data-ttu-id="1b61b-140">Adicione os seguintes registros à \_ tabela de validação para a tabela personalizada.</span><span class="sxs-lookup"><span data-stu-id="1b61b-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="1b61b-141">\_Tabela de validação</span><span class="sxs-lookup"><span data-stu-id="1b61b-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="1b61b-142">Tabela</span><span class="sxs-lookup"><span data-stu-id="1b61b-142">Table</span></span>              | <span data-ttu-id="1b61b-143">Coluna</span><span class="sxs-lookup"><span data-stu-id="1b61b-143">Column</span></span>     | <span data-ttu-id="1b61b-144">Nullable</span><span class="sxs-lookup"><span data-stu-id="1b61b-144">Nullable</span></span> | <span data-ttu-id="1b61b-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="1b61b-145">MinValue</span></span> | <span data-ttu-id="1b61b-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1b61b-146">MaxValue</span></span>   | <span data-ttu-id="1b61b-147">KeyTable</span><span class="sxs-lookup"><span data-stu-id="1b61b-147">KeyTable</span></span> | <span data-ttu-id="1b61b-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="1b61b-148">KeyColumn</span></span> | <span data-ttu-id="1b61b-149">Category</span><span class="sxs-lookup"><span data-stu-id="1b61b-149">Category</span></span>                     | <span data-ttu-id="1b61b-150">Definir</span><span class="sxs-lookup"><span data-stu-id="1b61b-150">Set</span></span> | <span data-ttu-id="1b61b-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b61b-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="1b61b-152">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="1b61b-152">CustomUserAccounts</span></span> | <span data-ttu-id="1b61b-153">UserName</span><span class="sxs-lookup"><span data-stu-id="1b61b-153">UserName</span></span>   | <span data-ttu-id="1b61b-154">N</span><span class="sxs-lookup"><span data-stu-id="1b61b-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="1b61b-155">Text</span><span class="sxs-lookup"><span data-stu-id="1b61b-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="1b61b-156">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="1b61b-156">CustomUserAccounts</span></span> | <span data-ttu-id="1b61b-157">Senha</span><span class="sxs-lookup"><span data-stu-id="1b61b-157">Password</span></span>   | <span data-ttu-id="1b61b-158">N</span><span class="sxs-lookup"><span data-stu-id="1b61b-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="1b61b-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="1b61b-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="1b61b-160">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="1b61b-160">CustomUserAccounts</span></span> | <span data-ttu-id="1b61b-161">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b61b-161">Attributes</span></span> | <span data-ttu-id="1b61b-162">S</span><span class="sxs-lookup"><span data-stu-id="1b61b-162">Y</span></span>        | <span data-ttu-id="1b61b-163">0</span><span class="sxs-lookup"><span data-stu-id="1b61b-163">0</span></span>        | <span data-ttu-id="1b61b-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="1b61b-164">2147483647</span></span> |          |           | <span data-ttu-id="1b61b-165">nulo</span><span class="sxs-lookup"><span data-stu-id="1b61b-165">null</span></span>                         |     |             |



 

<span data-ttu-id="1b61b-166">Continue a [criar as tabelas de erro e ActionText](authoring-the-actiontext-and-error-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1b61b-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



