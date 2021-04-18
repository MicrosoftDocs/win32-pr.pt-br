---
description: 'O método GetMediaTimes2 recupera os horários de início e de parada da mídia. Esse método é equivalente a IAMTimelineSrc:: GetMediaTimes, mas usa os valores de REFTIME.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'Método IAMTimelineSrc:: GetMediaTimes2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778472"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="114f7-104">Método IAMTimelineSrc:: GetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="114f7-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="114f7-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="114f7-105">\[Deprecated.</span></span> <span data-ttu-id="114f7-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="114f7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="114f7-107">O `GetMediaTimes2` método recupera os horários de início e de parada da mídia.</span><span class="sxs-lookup"><span data-stu-id="114f7-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="114f7-108">Esse método é equivalente a [**IAMTimelineSrc:: GetMediaTimes**](iamtimelinesrc-getmediatimes.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="114f7-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="114f7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="114f7-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="114f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="114f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114f7-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="114f7-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="114f7-112">Recebe a hora de início da mídia, em segundos.</span><span class="sxs-lookup"><span data-stu-id="114f7-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="114f7-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="114f7-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="114f7-114">Recebe a hora de parada da mídia, em segundos.</span><span class="sxs-lookup"><span data-stu-id="114f7-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114f7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="114f7-115">Return value</span></span>

<span data-ttu-id="114f7-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="114f7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="114f7-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="114f7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="114f7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="114f7-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="114f7-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="114f7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="114f7-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="114f7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="114f7-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="114f7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="114f7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="114f7-122">Requirements</span></span>



| <span data-ttu-id="114f7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="114f7-123">Requirement</span></span> | <span data-ttu-id="114f7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="114f7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="114f7-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="114f7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="114f7-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="114f7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="114f7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="114f7-127">Library</span></span><br/> | <dl> <span data-ttu-id="114f7-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="114f7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="114f7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="114f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114f7-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="114f7-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="114f7-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="114f7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




