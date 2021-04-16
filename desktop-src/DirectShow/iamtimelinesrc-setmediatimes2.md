---
description: 'O método SetMediaTimes2 define as horas de parada e de início da mídia. Esse método é equivalente a IAMTimelineSrc:: SetMediaTimes, mas usa os valores de REFTIME.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Método IAMTimelineSrc:: SetMediaTimes2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779849"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="6f824-104">Método IAMTimelineSrc:: SetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="6f824-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="6f824-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6f824-105">\[Deprecated.</span></span> <span data-ttu-id="6f824-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f824-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6f824-107">O `SetMediaTimes2` método define as horas de parada e de início da mídia.</span><span class="sxs-lookup"><span data-stu-id="6f824-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="6f824-108">Esse método é equivalente a [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="6f824-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f824-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f824-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="6f824-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f824-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f824-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="6f824-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="6f824-112">Hora de início da mídia, em segundos.</span><span class="sxs-lookup"><span data-stu-id="6f824-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="6f824-113">*Parar*</span><span class="sxs-lookup"><span data-stu-id="6f824-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="6f824-114">Hora de parada da mídia, em segundos.</span><span class="sxs-lookup"><span data-stu-id="6f824-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f824-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f824-115">Return value</span></span>

<span data-ttu-id="6f824-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f824-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f824-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f824-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f824-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f824-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f824-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6f824-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6f824-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6f824-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6f824-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6f824-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f824-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f824-122">Requirements</span></span>



| <span data-ttu-id="6f824-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f824-123">Requirement</span></span> | <span data-ttu-id="6f824-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6f824-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f824-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f824-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6f824-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f824-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6f824-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f824-127">Library</span></span><br/> | <dl> <span data-ttu-id="6f824-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f824-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f824-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f824-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f824-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="6f824-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="6f824-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6f824-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




