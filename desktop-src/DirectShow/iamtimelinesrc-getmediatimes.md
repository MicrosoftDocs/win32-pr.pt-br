---
description: O método GetMediaTimes recupera os horários de início e de parada da mídia.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Método IAMTimelineSrc:: GetMediaTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760086"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="d0ff8-103">Método IAMTimelineSrc:: GetMediaTimes</span><span class="sxs-lookup"><span data-stu-id="d0ff8-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="d0ff8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-104">\[Deprecated.</span></span> <span data-ttu-id="d0ff8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0ff8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0ff8-106">O `GetMediaTimes` método recupera os horários de início e de parada da mídia.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ff8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0ff8-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d0ff8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0ff8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ff8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="d0ff8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ff8-110">Recebe a hora de início da mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="d0ff8-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="d0ff8-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ff8-112">Recebe a hora de parada da mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ff8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0ff8-113">Return value</span></span>

<span data-ttu-id="d0ff8-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0ff8-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0ff8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ff8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0ff8-116">Remarks</span></span>

<span data-ttu-id="d0ff8-117">Os horários de mídia são relativos ao arquivo de mídia original.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="d0ff8-118">Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="d0ff8-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0ff8-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0ff8-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0ff8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0ff8-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0ff8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0ff8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ff8-122">Requirements</span></span>



| <span data-ttu-id="d0ff8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ff8-123">Requirement</span></span> | <span data-ttu-id="d0ff8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ff8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ff8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0ff8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0ff8-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ff8-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0ff8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0ff8-127">Library</span></span><br/> | <dl> <span data-ttu-id="d0ff8-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0ff8-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ff8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ff8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ff8-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="d0ff8-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d0ff8-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d0ff8-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




