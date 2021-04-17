---
description: O método Merge do objeto Database mescla o banco de dados de referência com o banco de dados base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Método Database. Merge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748597"
---
# <a name="databasemerge-method"></a><span data-ttu-id="5a9c0-103">Método Database. Merge</span><span class="sxs-lookup"><span data-stu-id="5a9c0-103">Database.Merge method</span></span>

<span data-ttu-id="5a9c0-104">O método **Merge** do objeto [**Database**](database-object.md) mescla o banco de dados de referência com o banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a9c0-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="5a9c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a9c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9c0-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="5a9c0-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9c0-108">O objeto de [**banco de dados**](database-object.md) necessário a ser mesclado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="5a9c0-109">*errotable*</span><span class="sxs-lookup"><span data-stu-id="5a9c0-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9c0-110">Um nome opcional de uma tabela para conter os nomes das tabelas que contêm conflitos de mesclagem, o número de linhas conflitantes dentro da tabela e uma referência à tabela com o conflito de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9c0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a9c0-111">Return value</span></span>

<span data-ttu-id="5a9c0-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9c0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a9c0-113">Remarks</span></span>

<span data-ttu-id="5a9c0-114">A função [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e o método **Merge** do objeto [**Database**](database-object.md) não podem ser usados para mesclar um módulo incluído em um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="5a9c0-115">Eles não devem ser usados para mesclar [módulos de mesclagem](merge-modules.md) em um pacote Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="5a9c0-116">Para incluir um módulo de mesclagem em um pacote de instalação, os autores de pacotes de instalação devem seguir as diretrizes descritas no tópico [aplicando módulos de mesclagem](applying-merge-modules.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9c0-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="5a9c0-117">O método **Merge** não copia [arquivos de gabinete](cabinet-files.md) inseridos ou [transformações incorporadas](embedded-transforms.md) do banco de dados de referência para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="5a9c0-118">Os fluxos de dados inseridos que estão listados na tabela [binária](binary-table.md) ou na [tabela de ícones](icon-table.md) são copiados do banco de dado de referência para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="5a9c0-119">Os armazenamentos inseridos no banco de dados de referência não são copiados para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="5a9c0-120">Se nenhuma tabela for fornecida, a mensagem de erro geral fornecerá o número de tabelas que contêm conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="5a9c0-121">Qualquer tabela pode ser passada, mas todas as outras colunas devem ser anuláveis porque a operação para atualizar a [tabela de erros](error-table.md) falhará se uma coluna não for anulável.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="5a9c0-122">Uma tabela recém-criada também pode ser passada porque o método **Merge** cria automaticamente as colunas que ele usa se forem encontrados conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="5a9c0-123">Duas colunas são usadas para apresentar conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="5a9c0-124">A primeira coluna é o nome da tabela e a coluna de chave primária.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="5a9c0-125">A segunda coluna é o número de linhas dessa tabela que têm falhas de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="5a9c0-126">Se as tabelas com o mesmo nome em ambos os bancos de dados não corresponderem no número de chaves primárias, nos tipos de coluna, no número de colunas ou nos nomes de coluna, o método de **mesclagem** falhará e lançará uma mensagem de erro informando o que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="5a9c0-127">Para que a tabela de erros permaneça, o manipulador de erros deve confirmar o banco de dados ao qual a tabela de erro pertence.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="5a9c0-128">No entanto, essa confirmação deve ser feita depois de usar a terceira coluna para obter as referências a essas tabelas em que ocorreram conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="5a9c0-129">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9c0-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9c0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a9c0-130">Requirements</span></span>



| <span data-ttu-id="5a9c0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a9c0-131">Requirement</span></span> | <span data-ttu-id="5a9c0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5a9c0-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9c0-133">Versão</span><span class="sxs-lookup"><span data-stu-id="5a9c0-133">Version</span></span><br/> | <span data-ttu-id="5a9c0-134">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5a9c0-135">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a9c0-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5a9c0-136">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a9c0-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5a9c0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5a9c0-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a9c0-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a9c0-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5a9c0-139">IID</span><span class="sxs-lookup"><span data-stu-id="5a9c0-139">IID</span></span><br/>     | <span data-ttu-id="5a9c0-140">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5a9c0-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




