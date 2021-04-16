---
description: O \_ método Get SrcHeight recupera a altura do retângulo de origem.
ms.assetid: 3c6647b3-dfca-490d-a3d5-9aa6988e387d
title: 'Método IDxtCompositor:: get_SrcHeight (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3ad874d7c02a9c9300af7fe3dbc69f6d351bba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779531"
---
# <a name="idxtcompositorget_srcheight-method"></a><span data-ttu-id="f794f-103">Método IDxtCompositor:: get \_ SrcHeight</span><span class="sxs-lookup"><span data-stu-id="f794f-103">IDxtCompositor::get\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="f794f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f794f-104">\[Deprecated.</span></span> <span data-ttu-id="f794f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f794f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f794f-106">O `get_SrcHeight` método recupera a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="f794f-106">The `get_SrcHeight` method retrieves the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f794f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f794f-107">Syntax</span></span>


```C++
HRESULT get_SrcHeight(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f794f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f794f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f794f-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f794f-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f794f-110">Recebe a altura do retângulo de origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="f794f-110">Receives the height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f794f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f794f-111">Return value</span></span>

<span data-ttu-id="f794f-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f794f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f794f-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f794f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f794f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f794f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f794f-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f794f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f794f-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f794f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f794f-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f794f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f794f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f794f-118">Requirements</span></span>



| <span data-ttu-id="f794f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f794f-119">Requirement</span></span> | <span data-ttu-id="f794f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f794f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f794f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f794f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f794f-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f794f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f794f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f794f-123">Library</span></span><br/> | <dl> <span data-ttu-id="f794f-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f794f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f794f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f794f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f794f-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="f794f-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




