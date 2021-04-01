---
title: Função SisFreeBackupStructure (Sisbkup. h)
description: Libera a estrutura de backup do SIS especificada.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Backup de função SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644448"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="a6324-104">Função SisFreeBackupStructure</span><span class="sxs-lookup"><span data-stu-id="a6324-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="a6324-105">A função **SisFreeBackupStructure** libera a estrutura de backup do SIS especificada.</span><span class="sxs-lookup"><span data-stu-id="a6324-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6324-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6324-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="a6324-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6324-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6324-108">*sisBackupStructure* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6324-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6324-109">Ponteiro para a estrutura de backup do SIS retornada de [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="a6324-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6324-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6324-110">Return value</span></span>

<span data-ttu-id="a6324-111">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a6324-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="a6324-112">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="a6324-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6324-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6324-113">Remarks</span></span>

<span data-ttu-id="a6324-114">Essa função deve ser chamada depois que a operação de backup for concluída para o volume identificado pelo valor do parâmetro *sisBackupStructure* .</span><span class="sxs-lookup"><span data-stu-id="a6324-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="a6324-115">Observe que não é seguro pressupor que isso apenas desaloque memória.</span><span class="sxs-lookup"><span data-stu-id="a6324-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="a6324-116">Por exemplo, essa função também pode executar operações administrativas adicionais para a arquitetura do SIS.</span><span class="sxs-lookup"><span data-stu-id="a6324-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="a6324-117">Portanto, chame essa função mesmo que sua operação de backup seja encerrada imediatamente depois.</span><span class="sxs-lookup"><span data-stu-id="a6324-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6324-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6324-118">Requirements</span></span>



| <span data-ttu-id="a6324-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6324-119">Requirement</span></span> | <span data-ttu-id="a6324-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6324-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6324-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6324-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6324-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6324-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a6324-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6324-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6324-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6324-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6324-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6324-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6324-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6324-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6324-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6324-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6324-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6324-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6324-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a6324-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6324-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6324-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6324-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6324-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6324-132">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="a6324-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

