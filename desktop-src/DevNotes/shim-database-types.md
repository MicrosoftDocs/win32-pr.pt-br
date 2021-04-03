---
description: Representa os tipos de bancos de dados de shims principal e personalizado.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipos de banco de dados Shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646193"
---
# <a name="shim-database-types"></a><span data-ttu-id="ee13c-103">Tipos de banco de dados Shim</span><span class="sxs-lookup"><span data-stu-id="ee13c-103">Shim Database Types</span></span>

<span data-ttu-id="ee13c-104">Representa os tipos de bancos de dados de shims principal e personalizado.</span><span class="sxs-lookup"><span data-stu-id="ee13c-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="ee13c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="ee13c-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="ee13c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee13c-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="ee13c-107"><dt>**Sdb \_ 0x80000000 \_ principal do banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="ee13c-108">O banco de dados principal.</span><span class="sxs-lookup"><span data-stu-id="ee13c-108">The main database.</span></span> <span data-ttu-id="ee13c-109">Se esse sinalizador não estiver presente, o banco de dados será um banco de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="ee13c-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="ee13c-110"><dt>**Sdb \_ 0x00010000 de \_ Shim de banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="ee13c-111">O banco de dados contém entradas de aplicativo a serem corrigido.</span><span class="sxs-lookup"><span data-stu-id="ee13c-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="ee13c-112"><dt>**Sdb \_ 0x00020000 \_ MSI do banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="ee13c-113">O banco de dados contém entradas MSI.</span><span class="sxs-lookup"><span data-stu-id="ee13c-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="ee13c-114"><dt>**Sdb \_ \_Drivers de banco de dados**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="ee13c-115">O banco de dados contém entradas de bloco de driver.</span><span class="sxs-lookup"><span data-stu-id="ee13c-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="ee13c-116"><dt>**Sdb \_ \_Detalhes do banco de dados**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="ee13c-117">O banco de dados contém detalhes de AppHelp.</span><span class="sxs-lookup"><span data-stu-id="ee13c-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="ee13c-118"><dt>**Sdb \_ \_ \_ Detalhes do Database SP**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="ee13c-119">O banco de dados contém os detalhes de AppHelp do SP.</span><span class="sxs-lookup"><span data-stu-id="ee13c-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="ee13c-120"><dt>**Sdb \_ 0x00200000 de \_ recurso do banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="ee13c-121">A DLL de recursos contém detalhes de AppHelp.</span><span class="sxs-lookup"><span data-stu-id="ee13c-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="ee13c-122"><dt>**Sdb \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0xF02F0000</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="ee13c-123">Uma máscara usada para extrair informações do banco de dados principal.</span><span class="sxs-lookup"><span data-stu-id="ee13c-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="ee13c-124"><dt>**\_Shim principal do banco de dados sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="ee13c-125">Banco \_ de dados sdb. \_ \| \_ \_ \| \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee13c-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="ee13c-126"><dt>**\_MSI principal do banco de dados sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="ee13c-127">banco de dados sdb do MSI do banco de dados SDB \_ \_ \| \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee13c-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="ee13c-128"><dt>**\_ \_ principais drivers do banco de dados sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="ee13c-129">banco de dados sdb. \_ \_ \| \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee13c-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="ee13c-130"><dt>**\_detalhes principais do banco de dados sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="ee13c-131">banco de dados sdb detalhes do banco de dados sdb \_ \_ \| \_ \_ principal</span><span class="sxs-lookup"><span data-stu-id="ee13c-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="ee13c-132"><dt>**\_ \_ detalhes principais do SP do banco de dados sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="ee13c-133">\_detalhes do SP do banco de dados sdb banco de \_ \_ \| \_ dados sdb \_ principal</span><span class="sxs-lookup"><span data-stu-id="ee13c-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="ee13c-134"><dt>**\_recurso principal do banco de dados sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee13c-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="ee13c-135">\_banco de \_ dados sdb de recurso de banco de dados sdb \| \_ \_ principal</span><span class="sxs-lookup"><span data-stu-id="ee13c-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="ee13c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee13c-136">Requirements</span></span>



| <span data-ttu-id="ee13c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee13c-137">Requirement</span></span> | <span data-ttu-id="ee13c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="ee13c-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee13c-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee13c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ee13c-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee13c-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee13c-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee13c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ee13c-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee13c-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee13c-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee13c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee13c-144">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="ee13c-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




