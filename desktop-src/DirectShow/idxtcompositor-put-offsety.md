---
description: O \_ método Put OffsetY especifica o deslocamento vertical do retângulo de destino.
ms.assetid: 68f2774d-9f26-4829-835d-b338c39f1c99
title: 'IDxtCompositor: método de ut_OffsetY de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a20c3812a1fb9756f01ae3a7eb684a6cf6ba0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785339"
---
# <a name="idxtcompositorput_offsety-method"></a><span data-ttu-id="4fef2-103">IDxtCompositor: método UT \_ OffsetY:p</span><span class="sxs-lookup"><span data-stu-id="4fef2-103">IDxtCompositor::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="4fef2-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4fef2-104">\[Deprecated.</span></span> <span data-ttu-id="4fef2-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4fef2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4fef2-106">O `put_OffsetY` método especifica o deslocamento vertical do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="4fef2-106">The `put_OffsetY` method specifies the vertical offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fef2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fef2-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4fef2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fef2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fef2-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4fef2-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fef2-110">O deslocamento vertical do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4fef2-110">The vertical offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fef2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4fef2-111">Return value</span></span>

<span data-ttu-id="4fef2-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4fef2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4fef2-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4fef2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fef2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fef2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4fef2-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4fef2-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4fef2-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4fef2-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4fef2-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4fef2-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fef2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fef2-118">Requirements</span></span>



| <span data-ttu-id="4fef2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fef2-119">Requirement</span></span> | <span data-ttu-id="4fef2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4fef2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fef2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fef2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4fef2-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fef2-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4fef2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fef2-123">Library</span></span><br/> | <dl> <span data-ttu-id="4fef2-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fef2-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fef2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fef2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fef2-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="4fef2-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




