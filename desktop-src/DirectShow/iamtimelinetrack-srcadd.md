---
description: O método SrcAdd adiciona uma origem à faixa.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Método IAMTimelineTrack:: SrcAdd (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780054"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="1868b-103">Método IAMTimelineTrack:: SrcAdd</span><span class="sxs-lookup"><span data-stu-id="1868b-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="1868b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1868b-104">\[Deprecated.</span></span> <span data-ttu-id="1868b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1868b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1868b-106">O `SrcAdd` método adiciona uma origem à faixa.</span><span class="sxs-lookup"><span data-stu-id="1868b-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="1868b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1868b-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="1868b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1868b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1868b-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="1868b-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="1868b-110">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="1868b-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1868b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1868b-111">Return value</span></span>

<span data-ttu-id="1868b-112">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1868b-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="1868b-113">Retorna E \_ nointerface se o objeto não for um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="1868b-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="1868b-114">Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="1868b-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1868b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1868b-115">Remarks</span></span>

<span data-ttu-id="1868b-116">Defina as horas de início e de término da origem antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="1868b-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="1868b-117">(Chamar [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md).)</span><span class="sxs-lookup"><span data-stu-id="1868b-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="1868b-118">Atualmente, o DES não pode renderizar simultaneamente mais de 75 fontes que foram compactadas com codecs do VCM (Gerenciador de compactação de vídeo).</span><span class="sxs-lookup"><span data-stu-id="1868b-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="1868b-119">Além disso, se o projeto como um todo contiver mais de 75 fontes, você deverá usar a reconexão dinâmica ou o DES não poderá visualizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="1868b-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="1868b-120">Para obter mais informações, consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="1868b-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="1868b-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1868b-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1868b-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1868b-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1868b-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1868b-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1868b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1868b-124">Requirements</span></span>



| <span data-ttu-id="1868b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1868b-125">Requirement</span></span> | <span data-ttu-id="1868b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1868b-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1868b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1868b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1868b-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1868b-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1868b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1868b-129">Library</span></span><br/> | <dl> <span data-ttu-id="1868b-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1868b-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1868b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1868b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1868b-132">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="1868b-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="1868b-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1868b-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




