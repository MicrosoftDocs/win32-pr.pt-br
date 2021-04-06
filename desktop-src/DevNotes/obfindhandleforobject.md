---
description: Recupera um identificador de objeto para o objeto especificado associado ao processo especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Função ObFindHandleForObject (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826224"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="07250-103">Função ObFindHandleForObject</span><span class="sxs-lookup"><span data-stu-id="07250-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="07250-104">\[Essa função é obsoleta e pode ser alterada ou indisponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="07250-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="07250-105">Evite usar essa função.\]</span><span class="sxs-lookup"><span data-stu-id="07250-105">Avoid using this function.\]</span></span>

<span data-ttu-id="07250-106">Recupera um identificador de objeto para o objeto especificado associado ao processo especificado.</span><span class="sxs-lookup"><span data-stu-id="07250-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="07250-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07250-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="07250-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07250-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07250-109">*Processo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07250-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07250-110">O processo.</span><span class="sxs-lookup"><span data-stu-id="07250-110">The process.</span></span> <span data-ttu-id="07250-111">Esse identificador é retornado pela função **IoGetCurrentProcess** ou **PsGetCurrentProcess** .</span><span class="sxs-lookup"><span data-stu-id="07250-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="07250-112">*Objeto* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07250-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07250-113">Um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="07250-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="07250-114">*Reserved1* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07250-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07250-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07250-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="07250-116">*Reserved2* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07250-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07250-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07250-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="07250-118">*Identificador* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="07250-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07250-119">O identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="07250-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07250-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07250-120">Return value</span></span>

<span data-ttu-id="07250-121">A função retornará **true** se uma correspondência for encontrada e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="07250-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07250-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="07250-122">Remarks</span></span>

<span data-ttu-id="07250-123">Essa função está disponível em Ntoskrnl.exe e pode ser chamada somente do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="07250-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="07250-124">A biblioteca de importação correspondente está disponível por meio do WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="07250-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="07250-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07250-125">Requirements</span></span>



| <span data-ttu-id="07250-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="07250-126">Requirement</span></span> | <span data-ttu-id="07250-127">Valor</span><span class="sxs-lookup"><span data-stu-id="07250-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07250-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07250-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07250-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="07250-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="07250-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07250-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07250-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07250-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07250-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07250-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="07250-133"><dt>Ntosp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07250-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="07250-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07250-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="07250-135"><dt>Ntoskrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07250-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




