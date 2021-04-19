---
description: 'O método SetCutPoint2 define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. Esse método é equivalente a IAMTimelineTrans:: SetCutPoint, mas usa um valor de REFTIME.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Método IAMTimelineTrans:: SetCutPoint2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779844"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="81ee2-104">Método IAMTimelineTrans:: SetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="81ee2-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="81ee2-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="81ee2-105">\[Deprecated.</span></span> <span data-ttu-id="81ee2-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81ee2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81ee2-107">O `SetCutPoint2` método define a hora em que a transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="81ee2-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="81ee2-108">Esse método é equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="81ee2-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ee2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81ee2-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="81ee2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81ee2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ee2-111">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="81ee2-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="81ee2-112">Recortar ponto em relação ao início da transição, em segundos.</span><span class="sxs-lookup"><span data-stu-id="81ee2-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ee2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81ee2-113">Return value</span></span>

<span data-ttu-id="81ee2-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81ee2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81ee2-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81ee2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ee2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="81ee2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81ee2-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="81ee2-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81ee2-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81ee2-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81ee2-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81ee2-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81ee2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ee2-120">Requirements</span></span>



| <span data-ttu-id="81ee2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ee2-121">Requirement</span></span> | <span data-ttu-id="81ee2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="81ee2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ee2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81ee2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="81ee2-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ee2-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81ee2-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81ee2-125">Library</span></span><br/> | <dl> <span data-ttu-id="81ee2-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81ee2-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ee2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="81ee2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ee2-128">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="81ee2-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="81ee2-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="81ee2-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




