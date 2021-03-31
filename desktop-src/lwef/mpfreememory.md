---
title: Função MpFreeMemory (MpClient. h)
description: Libera memória para o Gerenciador de proteção contra malware.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Recursos do ambiente Windows herdado da função MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644527"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="1ddb1-104">Função MpFreeMemory</span><span class="sxs-lookup"><span data-stu-id="1ddb1-104">MpFreeMemory function</span></span>

<span data-ttu-id="1ddb1-105">Libera memória para o Gerenciador de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="1ddb1-106">Todos os buffers alocados e retornados pelas funções de proteção contra malware devem ser liberados pelo chamador usando essa função.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddb1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ddb1-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="1ddb1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ddb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ddb1-109">*pMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ddb1-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ddb1-110">Tipo: **pVoid**</span><span class="sxs-lookup"><span data-stu-id="1ddb1-110">Type: **PVOID**</span></span>

<span data-ttu-id="1ddb1-111">Um ponteiro para a memória alocada por uma função de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ddb1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ddb1-112">Return value</span></span>

<span data-ttu-id="1ddb1-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ddb1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ddb1-114">Remarks</span></span>

<span data-ttu-id="1ddb1-115">Para facilitar o gerenciamento de memória para clientes, o Malware Protection Manager também define macros para liberar memória associada a várias estruturas retornadas pelas funções de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="1ddb1-116">As macros a seguir são definidas no arquivo de cabeçalho mpmemfree. h:</span><span class="sxs-lookup"><span data-stu-id="1ddb1-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="1ddb1-117">Name</span><span class="sxs-lookup"><span data-stu-id="1ddb1-117">Name</span></span>                            | <span data-ttu-id="1ddb1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ddb1-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1ddb1-119">\_informações \_ gratuitas do MPRESOURCE</span><span class="sxs-lookup"><span data-stu-id="1ddb1-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="1ddb1-120">Libera uma [**\_ informação MPRESOURCE**](mpresource-info.md)alocada.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="1ddb1-121">\_informações \_ gratuitas do MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="1ddb1-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="1ddb1-122">Libera uma [**\_ informação MPTHREAT**](mpthreat-info.md)alocada.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="1ddb1-123">\_informações localizadas do MPTHREAT \_ \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="1ddb1-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="1ddb1-124">Libera uma [**\_ \_ informação localizada de MPTHREAT**](mpthreat-localized-info.md)alocada.</span><span class="sxs-lookup"><span data-stu-id="1ddb1-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1ddb1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ddb1-125">Requirements</span></span>



| <span data-ttu-id="1ddb1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ddb1-126">Requirement</span></span> | <span data-ttu-id="1ddb1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1ddb1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddb1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ddb1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddb1-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ddb1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1ddb1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ddb1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddb1-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ddb1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ddb1-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ddb1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddb1-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ddb1-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ddb1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1ddb1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ddb1-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ddb1-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ddb1-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ddb1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddb1-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="1ddb1-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1ddb1-138">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="1ddb1-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="1ddb1-139">**informações de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="1ddb1-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="1ddb1-140">**\_informações localizadas do MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="1ddb1-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





