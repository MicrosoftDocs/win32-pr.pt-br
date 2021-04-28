---
description: 'Método IAMTimelineObj:: SetDirtyRange-não implementado.'
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: 'Método IAMTimelineObj:: SetDirtyRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3f70e5ba9d01733df154911c4f40d2b9d33776
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119484"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="a4df3-103">Método IAMTimelineObj:: SetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="a4df3-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="a4df3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a4df3-104">\[Deprecated.</span></span> <span data-ttu-id="a4df3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4df3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a4df3-106">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4df3-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4df3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4df3-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="a4df3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4df3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4df3-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="a4df3-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="a4df3-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a4df3-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a4df3-111">*Parar*</span><span class="sxs-lookup"><span data-stu-id="a4df3-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="a4df3-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a4df3-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4df3-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a4df3-113">Return value</span></span>

<span data-ttu-id="a4df3-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4df3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4df3-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4df3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4df3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4df3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4df3-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a4df3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4df3-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4df3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a4df3-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a4df3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4df3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4df3-120">Requirements</span></span>



| <span data-ttu-id="a4df3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4df3-121">Requirement</span></span> | <span data-ttu-id="a4df3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a4df3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4df3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4df3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a4df3-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4df3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a4df3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4df3-125">Library</span></span><br/> | <dl> <span data-ttu-id="a4df3-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4df3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4df3-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a4df3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4df3-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a4df3-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




