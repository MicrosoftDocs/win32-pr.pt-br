---
description: O método gettimen recupera a linha do tempo à qual esse grupo pertence.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'Método IAMTimelineGroup:: gettimeize (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770073"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="bff20-103">Método IAMTimelineGroup:: gettimen</span><span class="sxs-lookup"><span data-stu-id="bff20-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="bff20-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="bff20-104">\[Deprecated.</span></span> <span data-ttu-id="bff20-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bff20-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bff20-106">O `GetTimeline` método recupera a linha do tempo à qual esse grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="bff20-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff20-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bff20-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="bff20-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bff20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff20-109">*ppTimeline* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bff20-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bff20-110">Recebe a interface [**IAMTimeline**](iamtimeline.md) da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="bff20-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="bff20-111">Se o grupo não fizer parte de uma linha do tempo, o valor será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bff20-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff20-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bff20-112">Return value</span></span>

<span data-ttu-id="bff20-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bff20-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bff20-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bff20-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff20-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bff20-115">Remarks</span></span>

<span data-ttu-id="bff20-116">Se o valor retornado em *ppTimeline* não for **NULL**, a interface **IAMTimeline** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="bff20-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="bff20-117">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="bff20-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="bff20-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="bff20-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bff20-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bff20-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bff20-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bff20-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bff20-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bff20-121">Requirements</span></span>



| <span data-ttu-id="bff20-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff20-122">Requirement</span></span> | <span data-ttu-id="bff20-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bff20-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bff20-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bff20-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bff20-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff20-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bff20-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bff20-126">Library</span></span><br/> | <dl> <span data-ttu-id="bff20-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bff20-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff20-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bff20-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff20-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="bff20-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="bff20-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="bff20-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




