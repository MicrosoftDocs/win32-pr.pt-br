---
title: Função MpHandleClose (MpClient. h)
description: Fecha o identificador retornado por MpManagerOpen, MpScanStart, MpThreatOpen ou MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Recursos do ambiente Windows herdado da função MpHandleClose
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499700"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="1cbe9-104">Função MpHandleClose</span><span class="sxs-lookup"><span data-stu-id="1cbe9-104">MpHandleClose function</span></span>

<span data-ttu-id="1cbe9-105">Fecha o identificador retornado por [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)ou [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="1cbe9-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbe9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cbe9-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="1cbe9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cbe9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbe9-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbe9-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbe9-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="1cbe9-110">Identificador para fechar.</span><span class="sxs-lookup"><span data-stu-id="1cbe9-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cbe9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cbe9-111">Return value</span></span>

<span data-ttu-id="1cbe9-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-112">Type: **HRESULT**</span></span>

<span data-ttu-id="1cbe9-113">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cbe9-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="1cbe9-114">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="1cbe9-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="1cbe9-115">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1cbe9-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="1cbe9-116">O seguinte erro específico pode ser retornado pela função:</span><span class="sxs-lookup"><span data-stu-id="1cbe9-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="1cbe9-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1cbe9-117">Return Code</span></span>             | <span data-ttu-id="1cbe9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cbe9-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="1cbe9-119">E \_ Win \_ \_ identificador inválido</span><span class="sxs-lookup"><span data-stu-id="1cbe9-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="1cbe9-120">O identificador especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="1cbe9-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1cbe9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbe9-121">Requirements</span></span>



| <span data-ttu-id="1cbe9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbe9-122">Requirement</span></span> | <span data-ttu-id="1cbe9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1cbe9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbe9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cbe9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbe9-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1cbe9-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1cbe9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cbe9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbe9-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1cbe9-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1cbe9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cbe9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cbe9-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbe9-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cbe9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1cbe9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cbe9-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cbe9-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbe9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cbe9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbe9-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1cbe9-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="1cbe9-135">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="1cbe9-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="1cbe9-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





