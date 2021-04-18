---
description: 'Não há suporte. Chame o método IAMTimeline:: CreateEmptyNode para criar um novo objeto de linha do tempo. Depois que um objeto é criado, você não pode alterar seu tipo.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'Método IAMTimelineObj:: settimelinetype (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812981"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="40916-105">Método IAMTimelineObj:: settimelinetype</span><span class="sxs-lookup"><span data-stu-id="40916-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="40916-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="40916-106">\[Deprecated.</span></span> <span data-ttu-id="40916-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40916-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="40916-108">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="40916-108">Not supported.</span></span> <span data-ttu-id="40916-109">Chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) para criar um novo objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="40916-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="40916-110">Depois que um objeto é criado, você não pode alterar seu tipo.</span><span class="sxs-lookup"><span data-stu-id="40916-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="40916-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40916-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="40916-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40916-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40916-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="40916-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="40916-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="40916-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40916-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40916-115">Return value</span></span>

<span data-ttu-id="40916-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="40916-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40916-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40916-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40916-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="40916-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="40916-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="40916-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="40916-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="40916-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="40916-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="40916-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="40916-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40916-122">Requirements</span></span>



| <span data-ttu-id="40916-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="40916-123">Requirement</span></span> | <span data-ttu-id="40916-124">Valor</span><span class="sxs-lookup"><span data-stu-id="40916-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40916-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40916-125">Header</span></span><br/>  | <dl> <span data-ttu-id="40916-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="40916-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="40916-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40916-127">Library</span></span><br/> | <dl> <span data-ttu-id="40916-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40916-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40916-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="40916-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40916-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="40916-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




