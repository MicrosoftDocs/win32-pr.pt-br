---
title: Método IMsRdpClientNonScriptable6 SendLocation2D
description: Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendLocation2D
- Método SendLocation2D Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6, método SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103645610"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="07cd0-106">Método IMsRdpClientNonScriptable6:: SendLocation2D</span><span class="sxs-lookup"><span data-stu-id="07cd0-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="07cd0-107">Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="07cd0-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cd0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07cd0-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="07cd0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07cd0-109">Parameters</span></span>

<span data-ttu-id="07cd0-110">*latitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07cd0-110">*latitude* \[in\]</span></span>

<span data-ttu-id="07cd0-111">A latitude de uma localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="07cd0-111">The latitude of a geographic location.</span></span> <span data-ttu-id="07cd0-112">O intervalo válido de valores de latitude é de-90,0 a 90,0 graus.</span><span class="sxs-lookup"><span data-stu-id="07cd0-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="07cd0-113">*longitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07cd0-113">*longitude* \[in\]</span></span>

<span data-ttu-id="07cd0-114">A longitude de uma localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="07cd0-114">The longitude of a geographic location.</span></span> <span data-ttu-id="07cd0-115">O intervalo válido de valores de latitude é de-180,0 a 180,0 graus.</span><span class="sxs-lookup"><span data-stu-id="07cd0-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="07cd0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07cd0-116">Return value</span></span>

<span data-ttu-id="07cd0-117">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="07cd0-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cd0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07cd0-118">Requirements</span></span>

| <span data-ttu-id="07cd0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07cd0-119">Requirement</span></span> | <span data-ttu-id="07cd0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="07cd0-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="07cd0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07cd0-121">Minimum supported client</span></span>| <span data-ttu-id="07cd0-122">Windows 10, versão 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="07cd0-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="07cd0-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="07cd0-123">Type library</span></span>            | <span data-ttu-id="07cd0-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="07cd0-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="07cd0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="07cd0-125">DLL</span></span>                  | <span data-ttu-id="07cd0-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="07cd0-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="07cd0-127">IID</span><span class="sxs-lookup"><span data-stu-id="07cd0-127">IID</span></span>                      | <span data-ttu-id="07cd0-128">IID \_ IMsRdpClientNonScriptable6 é definido como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="07cd0-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="07cd0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="07cd0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cd0-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="07cd0-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
