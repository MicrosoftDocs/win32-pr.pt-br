---
description: O \_ método Get SrcOffsetX recupera o deslocamento horizontal do retângulo de origem.
ms.assetid: 528a5306-86bd-4ae2-ad03-57247362c5b5
title: 'Método IDxtCompositor:: get_SrcOffsetX (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ee116537061986a556854aed093b5e9a414016e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759123"
---
# <a name="idxtcompositorget_srcoffsetx-method"></a><span data-ttu-id="e0624-103">Método IDxtCompositor:: get \_ SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="e0624-103">IDxtCompositor::get\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="e0624-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e0624-104">\[Deprecated.</span></span> <span data-ttu-id="e0624-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0624-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0624-106">O `get_SrcOffsetX` método recupera o deslocamento horizontal do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="e0624-106">The `get_SrcOffsetX` method retrieves the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0624-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0624-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e0624-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0624-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0624-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e0624-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e0624-110">Recebe o deslocamento horizontal do retângulo de origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e0624-110">Receives the horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0624-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0624-111">Return value</span></span>

<span data-ttu-id="e0624-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e0624-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0624-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0624-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0624-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0624-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e0624-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e0624-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0624-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0624-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e0624-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e0624-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0624-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0624-118">Requirements</span></span>



| <span data-ttu-id="e0624-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0624-119">Requirement</span></span> | <span data-ttu-id="e0624-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e0624-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0624-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0624-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e0624-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0624-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e0624-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0624-123">Library</span></span><br/> | <dl> <span data-ttu-id="e0624-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0624-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0624-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0624-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0624-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="e0624-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




