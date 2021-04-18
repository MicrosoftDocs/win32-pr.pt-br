---
description: 'O método ModifyStopTime2 define a hora de parada. Esse método é equivalente a IAMTimelineSrc:: ModifyStopTime, mas usa um valor de REFTIME.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Método IAMTimelineSrc:: ModifyStopTime2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779850"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="4a2aa-104">Método IAMTimelineSrc:: ModifyStopTime2</span><span class="sxs-lookup"><span data-stu-id="4a2aa-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="4a2aa-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-105">\[Deprecated.</span></span> <span data-ttu-id="4a2aa-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a2aa-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a2aa-107">O `ModifyStopTime2` método define a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="4a2aa-108">Esse método é equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2aa-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2aa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a2aa-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4a2aa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a2aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2aa-111">*Parar*</span><span class="sxs-lookup"><span data-stu-id="4a2aa-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4a2aa-112">Nova hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2aa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a2aa-113">Return value</span></span>

<span data-ttu-id="4a2aa-114">Retornará S \_ OK se for bem-sucedido, ou E \_ INVALIDARG se a hora especificada não for válida.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2aa-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a2aa-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a2aa-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a2aa-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a2aa-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a2aa-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a2aa-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a2aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2aa-119">Requirements</span></span>



| <span data-ttu-id="4a2aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2aa-120">Requirement</span></span> | <span data-ttu-id="4a2aa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4a2aa-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2aa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a2aa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4a2aa-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2aa-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a2aa-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a2aa-124">Library</span></span><br/> | <dl> <span data-ttu-id="4a2aa-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a2aa-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2aa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a2aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2aa-127">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4a2aa-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4a2aa-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




