---
description: 'O método GetDuration2 recupera a duração da linha do tempo. Esse método é equivalente a IAMTimeline:: getDuration, mas usa um parâmetro do tipo Double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'Método IAMTimeline:: GetDuration2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748609"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="75c33-104">Método IAMTimeline:: GetDuration2</span><span class="sxs-lookup"><span data-stu-id="75c33-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="75c33-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="75c33-105">\[Deprecated.</span></span> <span data-ttu-id="75c33-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75c33-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="75c33-107">O `GetDuration2` método recupera a duração da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="75c33-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="75c33-108">Esse método é equivalente a [**IAMTimeline:: getDuration**](iamtimeline-getduration.md), mas usa um parâmetro do tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="75c33-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c33-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c33-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="75c33-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c33-111">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="75c33-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="75c33-112">Recebe a duração da linha do tempo, em segundos fracionários.</span><span class="sxs-lookup"><span data-stu-id="75c33-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c33-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75c33-113">Return value</span></span>

<span data-ttu-id="75c33-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75c33-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75c33-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75c33-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c33-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c33-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75c33-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="75c33-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="75c33-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="75c33-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="75c33-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="75c33-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75c33-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c33-120">Requirements</span></span>



| <span data-ttu-id="75c33-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c33-121">Requirement</span></span> | <span data-ttu-id="75c33-122">Valor</span><span class="sxs-lookup"><span data-stu-id="75c33-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c33-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75c33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="75c33-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c33-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="75c33-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75c33-125">Library</span></span><br/> | <dl> <span data-ttu-id="75c33-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75c33-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c33-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="75c33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c33-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="75c33-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="75c33-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="75c33-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




