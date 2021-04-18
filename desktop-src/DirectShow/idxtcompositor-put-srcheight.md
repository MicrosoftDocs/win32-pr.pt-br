---
description: O \_ método Put SrcHeight especifica a altura do retângulo de origem.
ms.assetid: 80c8cf92-36e2-4e57-8ce7-6a114bc8bab4
title: 'IDxtCompositor: método de ut_SrcHeight de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 80697a3c4a159256389f48273e66ca86547478fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766305"
---
# <a name="idxtcompositorput_srcheight-method"></a><span data-ttu-id="516ad-103">IDxtCompositor: método UT \_ SrcHeight:p</span><span class="sxs-lookup"><span data-stu-id="516ad-103">IDxtCompositor::put\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="516ad-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="516ad-104">\[Deprecated.</span></span> <span data-ttu-id="516ad-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="516ad-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="516ad-106">O `put_SrcHeight` método especifica a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="516ad-106">The `put_SrcHeight` method specifies the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="516ad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="516ad-107">Syntax</span></span>


```C++
HRESULT put_SrcHeight(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="516ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="516ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516ad-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="516ad-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516ad-110">A altura do retângulo de origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="516ad-110">The height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516ad-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="516ad-111">Return value</span></span>

<span data-ttu-id="516ad-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="516ad-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="516ad-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="516ad-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="516ad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="516ad-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="516ad-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="516ad-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="516ad-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="516ad-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="516ad-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="516ad-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="516ad-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="516ad-118">Requirements</span></span>



| <span data-ttu-id="516ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="516ad-119">Requirement</span></span> | <span data-ttu-id="516ad-120">Valor</span><span class="sxs-lookup"><span data-stu-id="516ad-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516ad-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="516ad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="516ad-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="516ad-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="516ad-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="516ad-123">Library</span></span><br/> | <dl> <span data-ttu-id="516ad-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="516ad-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516ad-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="516ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516ad-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="516ad-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




