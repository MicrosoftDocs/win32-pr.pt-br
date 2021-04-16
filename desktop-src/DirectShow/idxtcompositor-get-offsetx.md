---
description: O \_ método Get OffsetX recupera o deslocamento horizontal do retângulo de destino.
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'Método IDxtCompositor:: get_OffsetX (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779533"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="c79c6-103">Método IDxtCompositor:: get \_ OffsetX</span><span class="sxs-lookup"><span data-stu-id="c79c6-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="c79c6-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c79c6-104">\[Deprecated.</span></span> <span data-ttu-id="c79c6-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c79c6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c79c6-106">O `get_OffsetX` método recupera o deslocamento horizontal do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="c79c6-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c79c6-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c79c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c79c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79c6-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c79c6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c79c6-110">Recebe o deslocamento horizontal do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c79c6-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c79c6-111">Return value</span></span>

<span data-ttu-id="c79c6-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c79c6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c79c6-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c79c6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79c6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c79c6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c79c6-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c79c6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c79c6-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c79c6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c79c6-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c79c6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c79c6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c79c6-118">Requirements</span></span>



| <span data-ttu-id="c79c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79c6-119">Requirement</span></span> | <span data-ttu-id="c79c6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c79c6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c79c6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c79c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c79c6-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79c6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c79c6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c79c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="c79c6-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c79c6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c79c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79c6-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="c79c6-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




