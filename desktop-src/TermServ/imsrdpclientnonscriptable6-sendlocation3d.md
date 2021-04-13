---
title: Método IMsRdpClientNonScriptable6 SendLocation3D
description: Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendLocation3D
- Método SendLocation3D Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6, método SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456325"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="6c810-106">Método IMsRdpClientNonScriptable6:: SendLocation3D</span><span class="sxs-lookup"><span data-stu-id="6c810-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="6c810-107">Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="6c810-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c810-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c810-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="6c810-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c810-109">Parameters</span></span>

<span data-ttu-id="6c810-110">*latitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c810-110">*latitude* \[in\]</span></span>

<span data-ttu-id="6c810-111">A latitude de uma localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="6c810-111">The latitude of a geographic location.</span></span> <span data-ttu-id="6c810-112">O intervalo válido de valores de latitude é de-90,0 a 90,0 graus.</span><span class="sxs-lookup"><span data-stu-id="6c810-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="6c810-113">*longitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c810-113">*longitude* \[in\]</span></span>

<span data-ttu-id="6c810-114">A longitude de uma localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="6c810-114">The longitude of a geographic location.</span></span> <span data-ttu-id="6c810-115">O intervalo válido de valores de latitude é de-180,0 a 180,0 graus.</span><span class="sxs-lookup"><span data-stu-id="6c810-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="6c810-116">*altitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c810-116">*altitude* \[in\]</span></span>

<span data-ttu-id="6c810-117">A altitude de uma localização geográfica em metros.</span><span class="sxs-lookup"><span data-stu-id="6c810-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c810-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c810-118">Return value</span></span>

<span data-ttu-id="6c810-119">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6c810-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c810-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c810-120">Requirements</span></span>

| <span data-ttu-id="6c810-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c810-121">Requirement</span></span> | <span data-ttu-id="6c810-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6c810-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="6c810-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c810-123">Minimum supported client</span></span>| <span data-ttu-id="6c810-124">Windows 10, versão 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="6c810-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="6c810-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6c810-125">Type library</span></span>            | <span data-ttu-id="6c810-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6c810-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="6c810-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6c810-127">DLL</span></span>                  | <span data-ttu-id="6c810-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6c810-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="6c810-129">IID</span><span class="sxs-lookup"><span data-stu-id="6c810-129">IID</span></span>                      | <span data-ttu-id="6c810-130">IID \_ IMsRdpClientNonScriptable6 é definido como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="6c810-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="6c810-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c810-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c810-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="6c810-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
