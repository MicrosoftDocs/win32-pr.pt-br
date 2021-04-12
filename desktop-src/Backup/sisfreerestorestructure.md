---
title: Função SisFreeRestoreStructure (Sisbkup. h)
description: Libera a memória alocada para a estrutura de restauração do SIS especificada e executa tarefas que preparam o filtro SIS para configurar corretamente os links criados durante a operação de restauração.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Backup de função SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455817"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="f9453-104">Função SisFreeRestoreStructure</span><span class="sxs-lookup"><span data-stu-id="f9453-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="f9453-105">A função **SisFreeRestoreStructure** libera a memória alocada para a estrutura de restauração do SIS especificada e executa tarefas que preparam o filtro SIS para configurar corretamente os links criados durante a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="f9453-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9453-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9453-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="f9453-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9453-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9453-108">*sisRestoreStructure* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9453-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9453-109">Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="f9453-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9453-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9453-110">Return value</span></span>

<span data-ttu-id="f9453-111">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f9453-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="f9453-112">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="f9453-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9453-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9453-113">Remarks</span></span>

<span data-ttu-id="f9453-114">Acessar os links do SIS antes que a chamada para essa função seja concluída pode resultar em uma verificação de volume ou uma leitura parcial do conteúdo do link.</span><span class="sxs-lookup"><span data-stu-id="f9453-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="f9453-115">Observe que não é seguro pressupor que isso apenas desaloque memória.</span><span class="sxs-lookup"><span data-stu-id="f9453-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="f9453-116">Por exemplo, essa função também pode executar operações administrativas adicionais para a arquitetura do SIS.</span><span class="sxs-lookup"><span data-stu-id="f9453-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="f9453-117">Portanto, chame essa função mesmo se sua operação de restauração for encerrada imediatamente depois.</span><span class="sxs-lookup"><span data-stu-id="f9453-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9453-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9453-118">Requirements</span></span>



| <span data-ttu-id="f9453-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9453-119">Requirement</span></span> | <span data-ttu-id="f9453-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9453-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9453-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9453-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9453-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9453-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f9453-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9453-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9453-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9453-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f9453-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9453-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9453-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9453-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9453-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9453-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9453-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9453-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9453-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f9453-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9453-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9453-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9453-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9453-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9453-132">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="f9453-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

