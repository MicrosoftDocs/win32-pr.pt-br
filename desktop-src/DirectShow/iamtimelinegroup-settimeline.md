---
description: 'Não há suporte. Em vez disso, chame o método IAMTimeline:: addgroup.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'Método IAMTimelineGroup:: settimese (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785341"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="3fd29-104">Método IAMTimelineGroup:: settimese</span><span class="sxs-lookup"><span data-stu-id="3fd29-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="3fd29-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3fd29-105">\[Deprecated.</span></span> <span data-ttu-id="3fd29-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3fd29-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3fd29-107">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="3fd29-107">Not supported.</span></span> <span data-ttu-id="3fd29-108">Em vez disso, chame o método [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd29-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd29-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fd29-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="3fd29-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fd29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd29-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="3fd29-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd29-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3fd29-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd29-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fd29-113">Return value</span></span>

<span data-ttu-id="3fd29-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3fd29-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3fd29-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3fd29-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd29-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fd29-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3fd29-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3fd29-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3fd29-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3fd29-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3fd29-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3fd29-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fd29-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd29-120">Requirements</span></span>



| <span data-ttu-id="3fd29-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd29-121">Requirement</span></span> | <span data-ttu-id="3fd29-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3fd29-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd29-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fd29-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3fd29-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd29-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3fd29-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fd29-125">Library</span></span><br/> | <dl> <span data-ttu-id="3fd29-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fd29-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd29-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fd29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd29-128">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="3fd29-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




