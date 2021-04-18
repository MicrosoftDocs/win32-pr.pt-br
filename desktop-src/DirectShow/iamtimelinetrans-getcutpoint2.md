---
description: 'O método GetCutPoint2 recupera o ponto de recorte. Esse método é equivalente a IAMTimelineTrans:: GetCutPoint, mas usa um valor de REFTIME.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'Método IAMTimelineTrans:: GetCutPoint2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810392"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="8229f-104">Método IAMTimelineTrans:: GetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="8229f-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="8229f-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8229f-105">\[Deprecated.</span></span> <span data-ttu-id="8229f-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8229f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8229f-107">O `GetCutPoint2` método recupera o ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="8229f-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="8229f-108">Esse método é equivalente a [**IAMTimelineTrans:: GetCutPoint**](iamtimelinetrans-getcutpoint.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="8229f-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8229f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8229f-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="8229f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8229f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8229f-111">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="8229f-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="8229f-112">Recebe o ponto de recorte, em relação à hora de início da transição, em segundos.</span><span class="sxs-lookup"><span data-stu-id="8229f-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8229f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8229f-113">Return value</span></span>

<span data-ttu-id="8229f-114">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="8229f-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="8229f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8229f-115">Return code</span></span>                                                                               | <span data-ttu-id="8229f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8229f-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8229f-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="8229f-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="8229f-118">O ponto de recorte não foi definido.</span><span class="sxs-lookup"><span data-stu-id="8229f-118">The cut point was not set.</span></span> <span data-ttu-id="8229f-119">O valor retornado é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8229f-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="8229f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8229f-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8229f-121">O ponto de recorte foi definido com um valor diferente do padrão.</span><span class="sxs-lookup"><span data-stu-id="8229f-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="8229f-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8229f-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8229f-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="8229f-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="8229f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8229f-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8229f-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8229f-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8229f-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8229f-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8229f-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8229f-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8229f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8229f-128">Requirements</span></span>



| <span data-ttu-id="8229f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8229f-129">Requirement</span></span> | <span data-ttu-id="8229f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8229f-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8229f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8229f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8229f-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8229f-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8229f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8229f-133">Library</span></span><br/> | <dl> <span data-ttu-id="8229f-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8229f-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8229f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8229f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8229f-136">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="8229f-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="8229f-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8229f-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




