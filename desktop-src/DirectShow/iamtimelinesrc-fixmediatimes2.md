---
description: 'O método FixMediaTimes2 arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Esse método é equivalente a IAMTimelineSrc:: FixMediaTimes, mas usa os valores de REFTIME.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'Método IAMTimelineSrc:: FixMediaTimes2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810395"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="6091d-104">Método IAMTimelineSrc:: FixMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="6091d-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="6091d-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6091d-105">\[Deprecated.</span></span> <span data-ttu-id="6091d-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6091d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6091d-107">O `FixMediaTimes2` método arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída.</span><span class="sxs-lookup"><span data-stu-id="6091d-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="6091d-108">Esse método é equivalente a [**IAMTimelineSrc:: FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="6091d-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6091d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6091d-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6091d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6091d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6091d-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="6091d-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6091d-112">Ponteiro para uma variável que contém a hora de início, em segundos.</span><span class="sxs-lookup"><span data-stu-id="6091d-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="6091d-113">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="6091d-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="6091d-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="6091d-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6091d-115">Ponteiro para uma variável que contém a hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="6091d-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="6091d-116">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="6091d-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6091d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6091d-117">Return value</span></span>

<span data-ttu-id="6091d-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6091d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6091d-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6091d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6091d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6091d-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6091d-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6091d-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6091d-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6091d-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6091d-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6091d-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6091d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6091d-124">Requirements</span></span>



| <span data-ttu-id="6091d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6091d-125">Requirement</span></span> | <span data-ttu-id="6091d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6091d-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6091d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6091d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6091d-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6091d-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6091d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6091d-129">Library</span></span><br/> | <dl> <span data-ttu-id="6091d-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6091d-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6091d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6091d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6091d-132">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="6091d-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="6091d-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6091d-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




