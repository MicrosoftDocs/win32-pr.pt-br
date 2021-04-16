---
title: Função MpManagerVersionQuery (MpClient. h)
description: Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Recursos do ambiente Windows herdado da função MpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758144"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="e3849-104">Função MpManagerVersionQuery</span><span class="sxs-lookup"><span data-stu-id="e3849-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="e3849-105">Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="e3849-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3849-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3849-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e3849-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3849-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3849-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3849-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3849-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e3849-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="e3849-110">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="e3849-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="e3849-111">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="e3849-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e3849-112">*pVersionInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e3849-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3849-113">Tipo: **\_ informações de PMPVERSION**</span><span class="sxs-lookup"><span data-stu-id="e3849-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="e3849-114">Ponteiro para uma estrutura que contém informações de versão sobre vários componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="e3849-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="e3849-115">Consulte [**MPVERSION \_ info**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="e3849-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3849-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3849-116">Return value</span></span>

<span data-ttu-id="e3849-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3849-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e3849-118">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3849-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="e3849-119">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="e3849-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="e3849-120">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="e3849-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3849-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3849-121">Requirements</span></span>



| <span data-ttu-id="e3849-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3849-122">Requirement</span></span> | <span data-ttu-id="e3849-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e3849-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3849-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3849-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3849-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e3849-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e3849-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3849-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3849-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e3849-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3849-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3849-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3849-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3849-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3849-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e3849-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3849-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3849-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3849-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3849-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3849-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="e3849-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="e3849-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="e3849-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="e3849-135">**informações de MPVERSION \_**</span><span class="sxs-lookup"><span data-stu-id="e3849-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





