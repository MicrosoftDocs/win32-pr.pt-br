---
description: O método OpenDatabase do objeto instalador abre um banco de dados existente ou cria um novo, retornando um objeto de banco de dados. Ele gera um erro se o objeto de banco de dados não puder ser criado e aberto com êxito.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Método Installer. OpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492265"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="131fa-104">Método Installer. OpenDatabase</span><span class="sxs-lookup"><span data-stu-id="131fa-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="131fa-105">O método **OpenDatabase** do objeto [**instalador**](installer-object.md) abre um banco de dados existente ou cria um novo, retornando um objeto de [**banco de dados**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="131fa-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="131fa-106">Ele gera um erro se o objeto de **banco de dados** não puder ser criado e aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="131fa-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="131fa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="131fa-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="131fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="131fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="131fa-109">*name*</span><span class="sxs-lookup"><span data-stu-id="131fa-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="131fa-110">Cadeia de caracteres necessária que contém o nome do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="131fa-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="131fa-111">Se uma cadeia de caracteres vazia for fornecida, um banco de dados temporário será criado e não persistirá.</span><span class="sxs-lookup"><span data-stu-id="131fa-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="131fa-112">*OpenMode*</span><span class="sxs-lookup"><span data-stu-id="131fa-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="131fa-113">Um parâmetro da lista a seguir ou uma cadeia de caracteres que contém o nome do caminho do novo arquivo de banco de dados de saída que deve ser gravado após a confirmação.</span><span class="sxs-lookup"><span data-stu-id="131fa-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="131fa-114">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="131fa-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="131fa-115">Significado</span><span class="sxs-lookup"><span data-stu-id="131fa-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="131fa-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="131fa-117">Abre um banco de dados somente leitura, sem alterações persistentes.</span><span class="sxs-lookup"><span data-stu-id="131fa-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="131fa-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="131fa-119">Abre um banco de dados de leitura/gravação no modo de transação.</span><span class="sxs-lookup"><span data-stu-id="131fa-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="131fa-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="131fa-121">Abre uma leitura/gravação direta de banco de dados sem transação.</span><span class="sxs-lookup"><span data-stu-id="131fa-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="131fa-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="131fa-123">Cria um novo banco de dados, leitura/gravação de modo Transact.</span><span class="sxs-lookup"><span data-stu-id="131fa-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="131fa-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="131fa-125">Cria um novo banco de dados, modo direto de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="131fa-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="131fa-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="131fa-127">Abre um banco de dados para exibir arquivos de script de notificação, como os arquivos gerados pelo método [**CreateAdvertiseScript**](installer-createadvertisescript.md) .</span><span class="sxs-lookup"><span data-stu-id="131fa-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="131fa-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="131fa-129">Adiciona esse sinalizador para indicar um arquivo de patch.</span><span class="sxs-lookup"><span data-stu-id="131fa-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="131fa-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="131fa-130">Return value</span></span>

<span data-ttu-id="131fa-131">Um objeto de [**banco de dados**](database-object.md) que representa o banco de dados do instalador novo ou existente que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="131fa-131">A [**Database**](database-object.md) object that represents the existing or new installer database that was opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="131fa-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="131fa-132">Remarks</span></span>

<span data-ttu-id="131fa-133">Quando um banco de dados é aberto como a saída de outro banco de dados, o fluxo de informações de resumo do banco de dados de saída é, na verdade, um espelho somente leitura do banco de dados original e, portanto, não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="131fa-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="131fa-134">Além disso, ele não é persistido com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="131fa-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="131fa-135">Para criar ou modificar as informações de resumo do banco de dados de saída, ele deve ser fechado e reaberto.</span><span class="sxs-lookup"><span data-stu-id="131fa-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="131fa-136">Para fazer e salvar alterações em um banco de dados, primeiro abra o banco de dados na transação (msiOpenDatabaseModeTransact), crie (msiOpenDatabaseModeCreate ou msiOpenDatabaseModeCreateDirect) ou o modo direto (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="131fa-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="131fa-137">Depois de fazer as alterações, chame sempre o método [**Commit**](database-commit.md) antes de fechar o identificador do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="131fa-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="131fa-138">O método **Commit** libera todos os buffers.</span><span class="sxs-lookup"><span data-stu-id="131fa-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="131fa-139">Sempre chame o método [**Commit**](database-commit.md) em um banco de dados que tenha sido aberto no modo direto (MsiOpenDatabaseModeDirect ou msiOpenDatabaseModeCreateDirect) antes de fechar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="131fa-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="131fa-140">A falha em fazer isso pode corromper o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="131fa-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="131fa-141">Como o método **OpenDatabase** inicia o acesso ao banco de dados, ele não pode ser usado com uma instalação em execução.</span><span class="sxs-lookup"><span data-stu-id="131fa-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="131fa-142">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="131fa-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="131fa-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="131fa-143">Requirements</span></span>



| <span data-ttu-id="131fa-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="131fa-144">Requirement</span></span> | <span data-ttu-id="131fa-145">Valor</span><span class="sxs-lookup"><span data-stu-id="131fa-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="131fa-146">Versão</span><span class="sxs-lookup"><span data-stu-id="131fa-146">Version</span></span><br/> | <span data-ttu-id="131fa-147">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="131fa-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="131fa-148">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="131fa-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="131fa-149">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="131fa-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="131fa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="131fa-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="131fa-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="131fa-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="131fa-152">IID</span><span class="sxs-lookup"><span data-stu-id="131fa-152">IID</span></span><br/>     | <span data-ttu-id="131fa-153">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="131fa-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




