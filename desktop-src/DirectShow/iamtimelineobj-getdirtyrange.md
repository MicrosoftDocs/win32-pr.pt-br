---
description: 'Método IAMTimelineObj:: GetDirtyRange-sem suporte.'
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: 'Método IAMTimelineObj:: GetDirtyRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 828bb5a88d3bcefcf10f0a6e4f07070a4b60322d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098564"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="a1729-103">Método IAMTimelineObj:: GetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="a1729-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="a1729-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a1729-104">\[Deprecated.</span></span> <span data-ttu-id="a1729-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1729-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1729-106">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a1729-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1729-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1729-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="a1729-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1729-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1729-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="a1729-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a1729-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a1729-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1729-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="a1729-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a1729-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a1729-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1729-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a1729-113">Return value</span></span>

<span data-ttu-id="a1729-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a1729-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1729-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1729-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1729-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1729-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1729-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a1729-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1729-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1729-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1729-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1729-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1729-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1729-120">Requirements</span></span>



| <span data-ttu-id="a1729-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1729-121">Requirement</span></span> | <span data-ttu-id="a1729-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a1729-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1729-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1729-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1729-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1729-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1729-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1729-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1729-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1729-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1729-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1729-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1729-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a1729-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




