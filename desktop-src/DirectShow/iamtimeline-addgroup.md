---
description: O método addgroup adiciona um grupo à linha do tempo.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Método IAMTimeline:: addgroup (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768642"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="f1aac-103">Método IAMTimeline:: addgroup</span><span class="sxs-lookup"><span data-stu-id="f1aac-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="f1aac-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f1aac-104">\[Deprecated.</span></span> <span data-ttu-id="f1aac-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1aac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f1aac-106">O `AddGroup` método adiciona um grupo à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="f1aac-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1aac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1aac-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="f1aac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1aac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1aac-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="f1aac-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="f1aac-110">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do grupo.</span><span class="sxs-lookup"><span data-stu-id="f1aac-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1aac-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1aac-111">Return value</span></span>

<span data-ttu-id="f1aac-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="f1aac-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f1aac-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f1aac-113">Return code</span></span>                                                                                   | <span data-ttu-id="f1aac-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1aac-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f1aac-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1aac-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1aac-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f1aac-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="f1aac-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1aac-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f1aac-118">Número máximo de grupos excedido.</span><span class="sxs-lookup"><span data-stu-id="f1aac-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="f1aac-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="f1aac-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="f1aac-120">O objeto não é um grupo.</span><span class="sxs-lookup"><span data-stu-id="f1aac-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="f1aac-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1aac-121">Remarks</span></span>

<span data-ttu-id="f1aac-122">Atualmente, as linhas do tempo dão suporte a um máximo de 32 grupos.</span><span class="sxs-lookup"><span data-stu-id="f1aac-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="f1aac-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f1aac-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1aac-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1aac-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1aac-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f1aac-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1aac-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1aac-126">Requirements</span></span>



| <span data-ttu-id="f1aac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1aac-127">Requirement</span></span> | <span data-ttu-id="f1aac-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f1aac-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1aac-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1aac-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f1aac-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1aac-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f1aac-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1aac-131">Library</span></span><br/> | <dl> <span data-ttu-id="f1aac-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1aac-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1aac-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1aac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1aac-134">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="f1aac-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="f1aac-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f1aac-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




