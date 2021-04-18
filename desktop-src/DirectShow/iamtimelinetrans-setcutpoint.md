---
description: O método SetCutPoint define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Método IAMTimelineTrans:: SetCutPoint (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759908"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="a04c8-103">Método IAMTimelineTrans:: SetCutPoint</span><span class="sxs-lookup"><span data-stu-id="a04c8-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="a04c8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a04c8-104">\[Deprecated.</span></span> <span data-ttu-id="a04c8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a04c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a04c8-106">O `SetCutPoint` método define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="a04c8-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a04c8-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="a04c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a04c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04c8-109">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="a04c8-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a04c8-110">Recortar ponto em relação ao início da transição, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="a04c8-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="a04c8-111">Se o valor ficar fora dos limites da transição, ele será truncado para a hora válida mais próxima.</span><span class="sxs-lookup"><span data-stu-id="a04c8-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04c8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a04c8-112">Return value</span></span>

<span data-ttu-id="a04c8-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a04c8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a04c8-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a04c8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04c8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a04c8-115">Remarks</span></span>

<span data-ttu-id="a04c8-116">Por padrão, o ponto de recorte é o meio da transição.</span><span class="sxs-lookup"><span data-stu-id="a04c8-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="a04c8-117">Por exemplo, em uma transição que abrange um segundo, o ponto de recorte padrão é de 0,5 segundos na transição.</span><span class="sxs-lookup"><span data-stu-id="a04c8-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="a04c8-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a04c8-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a04c8-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a04c8-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a04c8-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a04c8-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a04c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a04c8-121">Requirements</span></span>



| <span data-ttu-id="a04c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04c8-122">Requirement</span></span> | <span data-ttu-id="a04c8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a04c8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a04c8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a04c8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a04c8-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04c8-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a04c8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a04c8-126">Library</span></span><br/> | <dl> <span data-ttu-id="a04c8-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a04c8-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04c8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a04c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04c8-129">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="a04c8-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a04c8-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="a04c8-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




