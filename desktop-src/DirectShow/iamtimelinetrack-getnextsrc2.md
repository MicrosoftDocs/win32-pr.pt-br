---
description: 'O método GetNextSrc2 pesquisa o roteiro para a próxima fonte que aparece na hora especificada ou posteriormente. Esse método é equivalente a IAMTimelineTrack:: GetNextSrc, mas usa um valor de REFTIME.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Método IAMTimelineTrack:: GetNextSrc2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784022"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="240e1-104">Método IAMTimelineTrack:: GetNextSrc2</span><span class="sxs-lookup"><span data-stu-id="240e1-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="240e1-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="240e1-105">\[Deprecated.</span></span> <span data-ttu-id="240e1-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="240e1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="240e1-107">O `GetNextSrc2` método pesquisa a próxima fonte que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="240e1-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="240e1-108">Esse método é equivalente a [**IAMTimelineTrack:: GetNextSrc**](iamtimelinetrack-getnextsrc.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="240e1-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="240e1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="240e1-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="240e1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="240e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="240e1-111">*ppSrc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="240e1-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="240e1-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="240e1-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="240e1-113">*Aquecimento*</span><span class="sxs-lookup"><span data-stu-id="240e1-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="240e1-114">Na entrada, contém a hora de início da pesquisa, em segundos.</span><span class="sxs-lookup"><span data-stu-id="240e1-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="240e1-115">Se o método recuperar uma origem, ele definirá o valor para a hora de parada da origem.</span><span class="sxs-lookup"><span data-stu-id="240e1-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="240e1-116">Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-la.</span><span class="sxs-lookup"><span data-stu-id="240e1-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="240e1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="240e1-117">Return value</span></span>

<span data-ttu-id="240e1-118">Retornará S \_ OK se o método recuperar uma origem, ou S \_ false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="240e1-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="240e1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="240e1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="240e1-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="240e1-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="240e1-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="240e1-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="240e1-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="240e1-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="240e1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="240e1-123">Requirements</span></span>



| <span data-ttu-id="240e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="240e1-124">Requirement</span></span> | <span data-ttu-id="240e1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="240e1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="240e1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="240e1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="240e1-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="240e1-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="240e1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="240e1-128">Library</span></span><br/> | <dl> <span data-ttu-id="240e1-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="240e1-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="240e1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="240e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240e1-131">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="240e1-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="240e1-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="240e1-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




