---
title: Função MpThreatEnumerate (MpClient. h)
description: Retorna informações sobre a próxima ameaça na lista de enumeração. Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Recursos do ambiente Windows herdado da função MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918816"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="dc112-105">Função MpThreatEnumerate</span><span class="sxs-lookup"><span data-stu-id="dc112-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="dc112-106">Retorna informações sobre a próxima ameaça na lista de enumeração.</span><span class="sxs-lookup"><span data-stu-id="dc112-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="dc112-107">Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.</span><span class="sxs-lookup"><span data-stu-id="dc112-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc112-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc112-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="dc112-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc112-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc112-110">*hThreatEnumHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dc112-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc112-111">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="dc112-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="dc112-112">Identificador para um contexto de enumeração de ameaça retornado por [**MpThreatOpen**](mpthreatopen.md).</span><span class="sxs-lookup"><span data-stu-id="dc112-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc112-113">*ppThreatInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc112-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc112-114">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="dc112-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="dc112-115">Retorna um ponteiro para uma estrutura de informações de ameaça, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="dc112-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="dc112-116">A estrutura contém informações como ID de ameaça, nome e severidade.</span><span class="sxs-lookup"><span data-stu-id="dc112-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc112-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc112-117">Return value</span></span>

<span data-ttu-id="dc112-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc112-118">Type: **HRESULT**</span></span>

<span data-ttu-id="dc112-119">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dc112-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="dc112-120">Se não houver mais itens para retornar, o valor de retorno será **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="dc112-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="dc112-121">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="dc112-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="dc112-122">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="dc112-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc112-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc112-123">Requirements</span></span>



| <span data-ttu-id="dc112-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc112-124">Requirement</span></span> | <span data-ttu-id="dc112-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dc112-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc112-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc112-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc112-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc112-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dc112-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc112-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc112-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc112-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc112-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc112-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc112-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc112-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc112-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dc112-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc112-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc112-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc112-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc112-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc112-135">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="dc112-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="dc112-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="dc112-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="dc112-137">**informações de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="dc112-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





