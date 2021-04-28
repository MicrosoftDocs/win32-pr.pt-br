---
description: 'Método IAMTimeline:: IsDirty-sem suporte.'
ms.assetid: ed6fd633-23b8-4b80-901c-d7b50fa4c15e
title: 'Método IAMTimeline:: IsDirty (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.IsDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ee51c44ae99a26e54a616da6752511f8a4e5f4a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119584"
---
# <a name="iamtimelineisdirty-method"></a><span data-ttu-id="b1701-103">Método IAMTimeline:: IsDirty</span><span class="sxs-lookup"><span data-stu-id="b1701-103">IAMTimeline::IsDirty method</span></span>

> [!Note]  
> <span data-ttu-id="b1701-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b1701-104">\[Deprecated.</span></span> <span data-ttu-id="b1701-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1701-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1701-106">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="b1701-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1701-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1701-107">Syntax</span></span>


```C++
HRESULT IsDirty(
   BOOL *pDirty
);
```



## <a name="parameters"></a><span data-ttu-id="b1701-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1701-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1701-109">*pDirty*</span><span class="sxs-lookup"><span data-stu-id="b1701-109">*pDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="b1701-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b1701-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1701-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1701-111">Return value</span></span>

<span data-ttu-id="b1701-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b1701-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1701-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1701-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1701-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1701-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1701-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b1701-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1701-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1701-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1701-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b1701-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1701-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1701-118">Requirements</span></span>



| <span data-ttu-id="b1701-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1701-119">Requirement</span></span> | <span data-ttu-id="b1701-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b1701-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1701-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1701-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b1701-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1701-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1701-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1701-123">Library</span></span><br/> | <dl> <span data-ttu-id="b1701-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1701-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1701-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b1701-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1701-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="b1701-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




