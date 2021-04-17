---
description: O \_ método Put SrcOffsetX especifica o deslocamento horizontal do retângulo de origem.
ms.assetid: 54f38dfd-3804-4ce4-ac70-5c7933e1a03f
title: 'IDxtCompositor: método de ut_SrcOffsetX de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a23cf2a07a209509cf55129ecd77ee8e035f5341
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758515"
---
# <a name="idxtcompositorput_srcoffsetx-method"></a><span data-ttu-id="2333e-103">IDxtCompositor: método UT \_ SrcOffsetX:p</span><span class="sxs-lookup"><span data-stu-id="2333e-103">IDxtCompositor::put\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="2333e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2333e-104">\[Deprecated.</span></span> <span data-ttu-id="2333e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2333e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2333e-106">O `put_SrcOffsetX` método especifica o deslocamento horizontal do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="2333e-106">The `put_SrcOffsetX` method specifies the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2333e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2333e-107">Syntax</span></span>


```C++
HRESULT put_SrcOffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="2333e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2333e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2333e-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2333e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2333e-110">O deslocamento horizontal do retângulo de origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="2333e-110">The horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2333e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2333e-111">Return value</span></span>

<span data-ttu-id="2333e-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2333e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2333e-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2333e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2333e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2333e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2333e-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="2333e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2333e-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2333e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2333e-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2333e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2333e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2333e-118">Requirements</span></span>



| <span data-ttu-id="2333e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2333e-119">Requirement</span></span> | <span data-ttu-id="2333e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2333e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2333e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2333e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2333e-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2333e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2333e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2333e-123">Library</span></span><br/> | <dl> <span data-ttu-id="2333e-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2333e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2333e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2333e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2333e-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="2333e-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




