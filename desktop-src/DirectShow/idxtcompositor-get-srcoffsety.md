---
description: O \_ método Get SrcOffsetY recupera o deslocamento vertical do retângulo de origem.
ms.assetid: b692e71b-c7a9-437c-9127-fa517e817883
title: 'Método IDxtCompositor:: get_SrcOffsetY (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fbe254037d35504a46aed519f1030a9d0aff0d02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812824"
---
# <a name="idxtcompositorget_srcoffsety-method"></a><span data-ttu-id="72eba-103">Método IDxtCompositor:: get \_ SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="72eba-103">IDxtCompositor::get\_SrcOffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="72eba-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="72eba-104">\[Deprecated.</span></span> <span data-ttu-id="72eba-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72eba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72eba-106">O `get_SrcOffsetY` método recupera o deslocamento vertical do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="72eba-106">The `get_SrcOffsetY` method retrieves the vertical offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="72eba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72eba-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="72eba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72eba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72eba-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="72eba-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="72eba-110">Recebe o deslocamento vertical do retângulo de origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="72eba-110">Receives the vertical offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72eba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72eba-111">Return value</span></span>

<span data-ttu-id="72eba-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72eba-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72eba-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72eba-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72eba-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="72eba-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72eba-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="72eba-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72eba-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72eba-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72eba-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72eba-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72eba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72eba-118">Requirements</span></span>



| <span data-ttu-id="72eba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="72eba-119">Requirement</span></span> | <span data-ttu-id="72eba-120">Valor</span><span class="sxs-lookup"><span data-stu-id="72eba-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72eba-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72eba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72eba-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="72eba-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72eba-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72eba-123">Library</span></span><br/> | <dl> <span data-ttu-id="72eba-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72eba-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72eba-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="72eba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72eba-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="72eba-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




