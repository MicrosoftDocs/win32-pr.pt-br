---
description: 'Saiba mais sobre: estrutura de JET_DBINFOUPGRADE'
title: Estrutura JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785512"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="ba6e6-103">Estrutura JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="ba6e6-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="ba6e6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ba6e6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="ba6e6-105">Estrutura JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="ba6e6-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="ba6e6-106">A estrutura de **JET_DBINFOUPGRADE** contém informações sobre o status de atualização do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="ba6e6-107">Esse valor será recuperado somente se **JET_DBINFOUPGRADE** foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e6-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="ba6e6-108">Essa estrutura não é necessária para as versões atuais do sistema operacional do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="ba6e6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ba6e6-109">Members</span></span>

<span data-ttu-id="ba6e6-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-110">**cbStruct**</span></span>

<span data-ttu-id="ba6e6-111">Defina como o tamanho da estrutura de **JET_DBINFOUPGRADE** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="ba6e6-112">**cbFilesizeLow**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="ba6e6-113">O **DWORD** baixo que reflete o tamanho de arquivo atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="ba6e6-114">**cbFilesizeHigh**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="ba6e6-115">O **DWORD** alto que reflete o tamanho do arquivo atual para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="ba6e6-116">**cbFreeSpaceRequiredLow**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="ba6e6-117">O menor **DWORD** do espaço livre em disco estimado necessário para uma atualização in-loco.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="ba6e6-118">**cbFreeSpaceRequiredHigh**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="ba6e6-119">O grande **DWORD** do espaço livre em disco estimado necessário para uma atualização in-loco.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="ba6e6-120">**csecToUpgrade**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-120">**csecToUpgrade**</span></span>

<span data-ttu-id="ba6e6-121">O tempo estimado necessário para a atualização, em segundos.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="ba6e6-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-122">**ulFlags**</span></span>

<span data-ttu-id="ba6e6-123">Um campo de bits formado por zero ou mais dos seguintes sinalizadores: **fUpgradable**, **fAlreadyUpgraded**.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="ba6e6-124">**fUpgradable**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-124">**fUpgradable**</span></span>

<span data-ttu-id="ba6e6-125">O banco de dados é atualizável.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-125">The database is upgradeable.</span></span>

<span data-ttu-id="ba6e6-126">**fAlreadyUpgraded**</span><span class="sxs-lookup"><span data-stu-id="ba6e6-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="ba6e6-127">O banco de dados é atualizado para o formato de banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="ba6e6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba6e6-128">Remarks</span></span>

<span data-ttu-id="ba6e6-129">Uma estrutura de **JET_DBINFOUPGRADE** é populada por uma chamada para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e6-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="ba6e6-130">Se a função não for concluída com sucesso, o conteúdo da estrutura será indefinido.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="ba6e6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba6e6-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba6e6-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ba6e6-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ba6e6-133">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba6e6-134"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ba6e6-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ba6e6-135">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba6e6-136"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ba6e6-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ba6e6-137">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ba6e6-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ba6e6-138">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ba6e6-138">See Also</span></span>

[<span data-ttu-id="ba6e6-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ba6e6-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ba6e6-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ba6e6-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ba6e6-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ba6e6-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ba6e6-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ba6e6-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ba6e6-143">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="ba6e6-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="ba6e6-144">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="ba6e6-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="ba6e6-145">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="ba6e6-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="ba6e6-146">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="ba6e6-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
