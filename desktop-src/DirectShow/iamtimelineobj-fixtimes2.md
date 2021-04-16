---
description: 'O método FixTimes2 arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai. Esse método é equivalente a IAMTimelineObj:: FixTimes, mas usa os valores de REFTIME.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Método IAMTimelineObj:: FixTimes2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758682"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="165b8-104">Método IAMTimelineObj:: FixTimes2</span><span class="sxs-lookup"><span data-stu-id="165b8-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="165b8-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="165b8-105">\[Deprecated.</span></span> <span data-ttu-id="165b8-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="165b8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="165b8-107">O `FixTimes2` método arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.</span><span class="sxs-lookup"><span data-stu-id="165b8-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="165b8-108">Esse método é equivalente a [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="165b8-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="165b8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="165b8-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="165b8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="165b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165b8-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="165b8-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="165b8-112">Ponteiro para uma variável que contém a hora de início, em segundos.</span><span class="sxs-lookup"><span data-stu-id="165b8-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="165b8-113">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="165b8-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="165b8-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="165b8-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="165b8-115">Ponteiro para uma variável que contém a hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="165b8-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="165b8-116">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="165b8-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165b8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="165b8-117">Return value</span></span>

<span data-ttu-id="165b8-118">Retornará S \_ OK se for bem-sucedido, ou E \_ NOTINTREE se o objeto não fizer parte de um grupo.</span><span class="sxs-lookup"><span data-stu-id="165b8-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="165b8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="165b8-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="165b8-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="165b8-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="165b8-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="165b8-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="165b8-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="165b8-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="165b8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="165b8-123">Requirements</span></span>



| <span data-ttu-id="165b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="165b8-124">Requirement</span></span> | <span data-ttu-id="165b8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="165b8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="165b8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="165b8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="165b8-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="165b8-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="165b8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="165b8-128">Library</span></span><br/> | <dl> <span data-ttu-id="165b8-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="165b8-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165b8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="165b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165b8-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="165b8-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="165b8-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="165b8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




