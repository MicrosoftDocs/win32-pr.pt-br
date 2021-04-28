---
description: 'Método IAMTimelineTrack:: MoveEverythingBy – não há suporte para esse método.'
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: 'Método IAMTimelineTrack:: MoveEverythingBy (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.MoveEverythingBy
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe85cf17c92c0809189e12e8ad40ceb1d1f3fd25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094584"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="5b447-103">Método IAMTimelineTrack:: MoveEverythingBy</span><span class="sxs-lookup"><span data-stu-id="5b447-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="5b447-104">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5b447-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b447-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b447-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="5b447-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b447-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b447-107">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="5b447-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="5b447-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5b447-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5b447-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="5b447-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="5b447-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5b447-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b447-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5b447-111">Return value</span></span>

<span data-ttu-id="5b447-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5b447-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b447-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b447-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b447-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b447-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5b447-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5b447-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5b447-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b447-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5b447-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5b447-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5b447-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b447-118">Requirements</span></span>



| <span data-ttu-id="5b447-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b447-119">Requirement</span></span> | <span data-ttu-id="5b447-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5b447-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b447-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b447-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5b447-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b447-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5b447-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b447-123">Library</span></span><br/> | <dl> <span data-ttu-id="5b447-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b447-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b447-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5b447-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b447-126">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="5b447-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 




