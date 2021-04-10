---
title: Estrutura de EDB_RSTMAP (Ntdsbcli. h)
description: Usado com a função DsRestoreRegister para mapear um banco de dados de backup para um novo banco de dados.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Estrutura de EDB_RSTMAP Active Directory
- Ponteiro de estrutura de PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009485"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="3643d-105">\_Estrutura RSTMAP EDB</span><span class="sxs-lookup"><span data-stu-id="3643d-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="3643d-106">A **estrutura \_ RSTMAP do EDB** é usada com a função [**DsRestoreRegister**](dsrestoreregister.md) para mapear um banco de dados de backup para um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3643d-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3643d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3643d-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="3643d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3643d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3643d-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="3643d-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="3643d-110">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do banco de dados em que foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="3643d-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="3643d-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="3643d-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="3643d-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo nome do banco de dados, incluindo seu novo local, quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="3643d-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3643d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3643d-113">Requirements</span></span>



| <span data-ttu-id="3643d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3643d-114">Requirement</span></span> | <span data-ttu-id="3643d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3643d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3643d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3643d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3643d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3643d-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="3643d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3643d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3643d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3643d-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="3643d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3643d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3643d-121"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="3643d-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="3643d-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3643d-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3643d-123">**EDB \_ RSTMAPW** (Unicode) e **\_ RSTMAPA EDB** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3643d-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="3643d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3643d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3643d-125">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="3643d-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="3643d-126">Estruturas de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="3643d-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





