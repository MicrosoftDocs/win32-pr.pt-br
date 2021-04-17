---
description: O método GetNextSrc pesquisa o roteiro para a próxima fonte que aparece na hora especificada ou posteriormente.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Método IAMTimelineTrack:: GetNextSrc (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766306"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="7b792-103">Método IAMTimelineTrack:: GetNextSrc</span><span class="sxs-lookup"><span data-stu-id="7b792-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="7b792-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7b792-104">\[Deprecated.</span></span> <span data-ttu-id="7b792-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b792-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b792-106">O `GetNextSrc` método pesquisa a próxima fonte que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7b792-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b792-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b792-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="7b792-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b792-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b792-109">*ppSrc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b792-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b792-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="7b792-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7b792-111">*Aquecimento*</span><span class="sxs-lookup"><span data-stu-id="7b792-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="7b792-112">Ponteiro para uma variável que contém a hora de início da pesquisa, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="7b792-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="7b792-113">Se o método recuperar uma origem, ele definirá o valor para a hora de parada da origem.</span><span class="sxs-lookup"><span data-stu-id="7b792-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="7b792-114">Se o método não recuperar uma origem, o valor se tornará inválido e o aplicativo não deverá usá-la.</span><span class="sxs-lookup"><span data-stu-id="7b792-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b792-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b792-115">Return value</span></span>

<span data-ttu-id="7b792-116">Retornará S \_ OK se o método recuperar uma origem, ou S \_ false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7b792-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b792-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b792-117">Remarks</span></span>

<span data-ttu-id="7b792-118">Se o tempo especificado por *pinagem* estiver entre as horas de início e de parada de uma origem, o método recuperará essa fonte.</span><span class="sxs-lookup"><span data-stu-id="7b792-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="7b792-119">Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="7b792-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="7b792-120">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="7b792-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="7b792-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7b792-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b792-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b792-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7b792-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7b792-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b792-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b792-124">Requirements</span></span>



| <span data-ttu-id="7b792-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b792-125">Requirement</span></span> | <span data-ttu-id="7b792-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7b792-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b792-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b792-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7b792-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b792-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7b792-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b792-129">Library</span></span><br/> | <dl> <span data-ttu-id="7b792-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b792-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b792-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b792-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b792-132">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="7b792-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="7b792-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7b792-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




