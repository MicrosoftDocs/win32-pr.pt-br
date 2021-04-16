---
description: O método GetNextSrcEx recupera a próxima fonte após a origem especificada.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Método IAMTimelineTrack:: GetNextSrcEx (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757885"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="c4e8a-103">Método IAMTimelineTrack:: GetNextSrcEx</span><span class="sxs-lookup"><span data-stu-id="c4e8a-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="c4e8a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-104">\[Deprecated.</span></span> <span data-ttu-id="c4e8a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4e8a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4e8a-106">O `GetNextSrcEx` método recupera a próxima fonte após a origem especificada.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e8a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4e8a-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="c4e8a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4e8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e8a-109">*pLast*</span><span class="sxs-lookup"><span data-stu-id="c4e8a-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="c4e8a-110">Ponteiro para o objeto de origem anterior ou **NULL** para recuperar a primeira origem na faixa.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="c4e8a-111">*ppNext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4e8a-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e8a-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do próximo objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e8a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4e8a-113">Return value</span></span>

<span data-ttu-id="c4e8a-114">Retornará S \_ OK se o método recuperar uma origem, ou S \_ false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e8a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4e8a-115">Remarks</span></span>

<span data-ttu-id="c4e8a-116">Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="c4e8a-117">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="c4e8a-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c4e8a-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4e8a-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c4e8a-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c4e8a-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4e8a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4e8a-121">Requirements</span></span>



| <span data-ttu-id="c4e8a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4e8a-122">Requirement</span></span> | <span data-ttu-id="c4e8a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c4e8a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e8a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4e8a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c4e8a-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e8a-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c4e8a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4e8a-126">Library</span></span><br/> | <dl> <span data-ttu-id="c4e8a-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4e8a-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e8a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4e8a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e8a-129">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="c4e8a-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="c4e8a-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c4e8a-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




