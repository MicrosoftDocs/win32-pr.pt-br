---
description: O \_ método Put altura especifica a altura do retângulo de destino.
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: 'IDxtCompositor: método de ut_Height de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757290"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="da2ae-103">IDxtCompositor::p método de altura de UT \_</span><span class="sxs-lookup"><span data-stu-id="da2ae-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="da2ae-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="da2ae-104">\[Deprecated.</span></span> <span data-ttu-id="da2ae-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da2ae-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da2ae-106">O `put_Height` método especifica a altura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="da2ae-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2ae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da2ae-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="da2ae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da2ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2ae-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da2ae-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2ae-110">A altura do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="da2ae-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2ae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da2ae-111">Return value</span></span>

<span data-ttu-id="da2ae-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="da2ae-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da2ae-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da2ae-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da2ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="da2ae-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da2ae-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="da2ae-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="da2ae-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="da2ae-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da2ae-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="da2ae-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da2ae-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da2ae-118">Requirements</span></span>



| <span data-ttu-id="da2ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da2ae-119">Requirement</span></span> | <span data-ttu-id="da2ae-120">Valor</span><span class="sxs-lookup"><span data-stu-id="da2ae-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da2ae-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da2ae-121">Header</span></span><br/>  | <dl> <span data-ttu-id="da2ae-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2ae-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="da2ae-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da2ae-123">Library</span></span><br/> | <dl> <span data-ttu-id="da2ae-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da2ae-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da2ae-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="da2ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2ae-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="da2ae-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




