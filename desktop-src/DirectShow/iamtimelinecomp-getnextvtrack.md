---
description: O método GetNextVTrack recupera a próxima faixa virtual após uma faixa virtual especificada.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Método IAMTimelineComp:: GetNextVTrack (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785344"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="5462e-103">Método IAMTimelineComp:: GetNextVTrack</span><span class="sxs-lookup"><span data-stu-id="5462e-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="5462e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5462e-104">\[Deprecated.</span></span> <span data-ttu-id="5462e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5462e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5462e-106">O `GetNextVTrack` método recupera a próxima faixa virtual após uma faixa virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="5462e-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="5462e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5462e-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="5462e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5462e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5462e-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="5462e-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="5462e-110">Ponteiro para o controle virtual anterior ou **NULL** para recuperar a primeira faixa virtual na composição.</span><span class="sxs-lookup"><span data-stu-id="5462e-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="5462e-111">*ppNextVirtualTrack* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5462e-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5462e-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do próximo controle virtual, em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="5462e-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5462e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5462e-113">Return value</span></span>

<span data-ttu-id="5462e-114">Retornará S \_ OK se o método recuperar uma faixa virtual ou, \_ caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="5462e-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5462e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5462e-115">Remarks</span></span>

<span data-ttu-id="5462e-116">Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="5462e-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="5462e-117">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="5462e-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="5462e-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5462e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5462e-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5462e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5462e-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5462e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5462e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5462e-121">Requirements</span></span>



| <span data-ttu-id="5462e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5462e-122">Requirement</span></span> | <span data-ttu-id="5462e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5462e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5462e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5462e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5462e-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5462e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5462e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5462e-126">Library</span></span><br/> | <dl> <span data-ttu-id="5462e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5462e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5462e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5462e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5462e-129">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="5462e-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="5462e-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5462e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




