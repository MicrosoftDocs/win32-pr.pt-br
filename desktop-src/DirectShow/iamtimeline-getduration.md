---
description: O método GetDuration recupera a duração da linha do tempo.
ms.assetid: d60269b8-597a-4ba4-932a-54b4a36e9a7a
title: 'Método IAMTimeline:: getDuration (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98257c40bf2072a2b8881a4744cdbe6d3a4e7df5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754252"
---
# <a name="iamtimelinegetduration-method"></a><span data-ttu-id="28ce4-103">Método IAMTimeline:: getDuration</span><span class="sxs-lookup"><span data-stu-id="28ce4-103">IAMTimeline::GetDuration method</span></span>

> [!Note]  
> <span data-ttu-id="28ce4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="28ce4-104">\[Deprecated.</span></span> <span data-ttu-id="28ce4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28ce4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="28ce4-106">O `GetDuration` método recupera a duração da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="28ce4-106">The `GetDuration` method retrieves the duration of the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ce4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28ce4-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   REFERENCE_TIME *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="28ce4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28ce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ce4-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="28ce4-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="28ce4-110">Recebe a duração da linha do tempo, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="28ce4-110">Receives the duration of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ce4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28ce4-111">Return value</span></span>

<span data-ttu-id="28ce4-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="28ce4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28ce4-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28ce4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ce4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="28ce4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="28ce4-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="28ce4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="28ce4-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="28ce4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="28ce4-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="28ce4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28ce4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ce4-118">Requirements</span></span>



| <span data-ttu-id="28ce4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ce4-119">Requirement</span></span> | <span data-ttu-id="28ce4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="28ce4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28ce4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28ce4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="28ce4-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ce4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="28ce4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28ce4-123">Library</span></span><br/> | <dl> <span data-ttu-id="28ce4-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ce4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ce4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="28ce4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ce4-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="28ce4-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="28ce4-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="28ce4-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




