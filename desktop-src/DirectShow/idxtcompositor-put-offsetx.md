---
description: O \_ método Put OffsetX especifica o deslocamento horizontal do retângulo de destino.
ms.assetid: 057919e1-d65f-487d-b5d7-1c43967ce66d
title: 'IDxtCompositor: método de ut_OffsetX de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05fe43db86e266ba9ddec32ebd0fd4d59c3df398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757679"
---
# <a name="idxtcompositorput_offsetx-method"></a><span data-ttu-id="137b7-103">IDxtCompositor: método UT \_ OffsetX:p</span><span class="sxs-lookup"><span data-stu-id="137b7-103">IDxtCompositor::put\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="137b7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="137b7-104">\[Deprecated.</span></span> <span data-ttu-id="137b7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="137b7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="137b7-106">O `put_OffsetX` método especifica o deslocamento horizontal do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="137b7-106">The `put_OffsetX` method specifies the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="137b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="137b7-107">Syntax</span></span>


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="137b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="137b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="137b7-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="137b7-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="137b7-110">O deslocamento horizontal do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="137b7-110">The horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="137b7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="137b7-111">Return value</span></span>

<span data-ttu-id="137b7-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="137b7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="137b7-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="137b7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="137b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="137b7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="137b7-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="137b7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="137b7-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="137b7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="137b7-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="137b7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="137b7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="137b7-118">Requirements</span></span>



| <span data-ttu-id="137b7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="137b7-119">Requirement</span></span> | <span data-ttu-id="137b7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="137b7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="137b7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="137b7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="137b7-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="137b7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="137b7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="137b7-123">Library</span></span><br/> | <dl> <span data-ttu-id="137b7-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="137b7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="137b7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="137b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137b7-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="137b7-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




