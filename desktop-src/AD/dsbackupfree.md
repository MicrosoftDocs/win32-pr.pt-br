---
title: Função DsBackupFree (Ntdsbcli. h)
description: Libera a memória alocada pelas funções de backup e restauração Active Directory Domain Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Função DsBackupFree Active Directory
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824346"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="22c4d-104">Função DsBackupFree</span><span class="sxs-lookup"><span data-stu-id="22c4d-104">DsBackupFree function</span></span>

<span data-ttu-id="22c4d-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="22c4d-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22c4d-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="22c4d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="22c4d-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="22c4d-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="22c4d-108">A função **DsBackupFree** libera a memória alocada pelas funções de backup e restauração de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="22c4d-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="22c4d-109">As funções a seguir alocam memória que deve ser liberada com a função **DsBackupFree** .</span><span class="sxs-lookup"><span data-stu-id="22c4d-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="22c4d-110">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="22c4d-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="22c4d-111">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="22c4d-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="22c4d-112">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="22c4d-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="22c4d-113">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="22c4d-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="22c4d-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22c4d-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="22c4d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22c4d-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c4d-116">*pvBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22c4d-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c4d-117">Ponteiro para o buffer de memória a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="22c4d-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c4d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22c4d-118">Return value</span></span>

<span data-ttu-id="22c4d-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="22c4d-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c4d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c4d-120">Requirements</span></span>



| <span data-ttu-id="22c4d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c4d-121">Requirement</span></span> | <span data-ttu-id="22c4d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="22c4d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c4d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c4d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22c4d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c4d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22c4d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c4d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22c4d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22c4d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22c4d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22c4d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c4d-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c4d-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="22c4d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22c4d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="22c4d-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22c4d-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="22c4d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="22c4d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c4d-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c4d-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c4d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="22c4d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c4d-134">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="22c4d-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="22c4d-135">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="22c4d-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="22c4d-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="22c4d-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="22c4d-137">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="22c4d-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="22c4d-138">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="22c4d-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="22c4d-139">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="22c4d-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

