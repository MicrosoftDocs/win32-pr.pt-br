---
description: O método GetCutsOnly determina se a transição é renderizada como um recorte. Nesse caso, a transição ocorre instantaneamente no ponto de recorte.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Método IAMTimelineTrans:: GetCutsOnly (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782841"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="05053-104">Método IAMTimelineTrans:: GetCutsOnly</span><span class="sxs-lookup"><span data-stu-id="05053-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="05053-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="05053-105">\[Deprecated.</span></span> <span data-ttu-id="05053-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05053-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05053-107">O `GetCutsOnly` método determina se a transição é renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="05053-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="05053-108">Nesse caso, a transição ocorre instantaneamente no ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="05053-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="05053-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05053-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="05053-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05053-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05053-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="05053-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="05053-112">Recebe um valor booliano que especifica se a transição é renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="05053-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="05053-113">Se for **true**, a transição será uma recorte instantânea.</span><span class="sxs-lookup"><span data-stu-id="05053-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="05053-114">Se **for false**, a transição ocorrerá durante sua duração normal.</span><span class="sxs-lookup"><span data-stu-id="05053-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05053-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05053-115">Return value</span></span>

<span data-ttu-id="05053-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="05053-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05053-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05053-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05053-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="05053-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05053-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="05053-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05053-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05053-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05053-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="05053-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05053-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05053-122">Requirements</span></span>



| <span data-ttu-id="05053-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="05053-123">Requirement</span></span> | <span data-ttu-id="05053-124">Valor</span><span class="sxs-lookup"><span data-stu-id="05053-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05053-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05053-125">Header</span></span><br/>  | <dl> <span data-ttu-id="05053-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="05053-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05053-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05053-127">Library</span></span><br/> | <dl> <span data-ttu-id="05053-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05053-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05053-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="05053-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05053-130">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="05053-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="05053-131">**IAMTimelineTrans::SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="05053-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="05053-132">**IAMTimelineTrans::GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="05053-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="05053-133">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="05053-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="05053-134">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="05053-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




