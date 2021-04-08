---
title: Função SisFreeAllocatedMemory (Sisbkup. h)
description: Libera memória alocada pelas funções de API do SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Backup de função SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824274"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="bf2e8-104">Função SisFreeAllocatedMemory</span><span class="sxs-lookup"><span data-stu-id="bf2e8-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="bf2e8-105">A função **SisFreeAllocatedMemory** libera a memória alocada pelas funções de API do SIS.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2e8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf2e8-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="bf2e8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf2e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2e8-108">*allocatedSpace* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-109">Ponteiro para a memória alocada pela API do SIS.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2e8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf2e8-110">Return value</span></span>

<span data-ttu-id="bf2e8-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2e8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf2e8-112">Remarks</span></span>

<span data-ttu-id="bf2e8-113">Depois que a chamada para essa função for concluída, o chamador poderá não acessar mais a memória liberada.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="bf2e8-114">Essa chamada deve ser usada para desalocar a memória alocada para as cadeias de caracteres de parâmetro *commonStoreRootPathname* retornadas de [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md), e a matriz de cadeias de caracteres que contém nomes de arquivo de repositório comum retornado de **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md).</span><span class="sxs-lookup"><span data-stu-id="bf2e8-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="bf2e8-115">No último caso, a própria matriz também deve ser liberada chamando **SisFreeAllocatedMemory**.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2e8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2e8-116">Requirements</span></span>



| <span data-ttu-id="bf2e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2e8-117">Requirement</span></span> | <span data-ttu-id="bf2e8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2e8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2e8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf2e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2e8-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bf2e8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf2e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2e8-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf2e8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf2e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2e8-124"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf2e8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf2e8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf2e8-126"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf2e8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2e8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf2e8-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2e8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf2e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2e8-130">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-131">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-132">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-133">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





