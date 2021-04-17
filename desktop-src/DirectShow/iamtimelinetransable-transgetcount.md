---
description: O método TransGetCount recupera o número de transições neste objeto.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'Método IAMTimelineTransable:: TransGetCount (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81b5fc6301b319b8716a6db25fce2b1e5c2d4961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792548"
---
# <a name="iamtimelinetransabletransgetcount-method"></a><span data-ttu-id="75eb1-103">Método IAMTimelineTransable:: TransGetCount</span><span class="sxs-lookup"><span data-stu-id="75eb1-103">IAMTimelineTransable::TransGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="75eb1-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="75eb1-104">\[Deprecated.</span></span> <span data-ttu-id="75eb1-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75eb1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="75eb1-106">O `TransGetCount` método recupera o número de transições neste objeto.</span><span class="sxs-lookup"><span data-stu-id="75eb1-106">The `TransGetCount` method retrieves the number of transitions on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75eb1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75eb1-107">Syntax</span></span>


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="75eb1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75eb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75eb1-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="75eb1-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="75eb1-110">Recebe o número de transições.</span><span class="sxs-lookup"><span data-stu-id="75eb1-110">Receives the number of transitions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75eb1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75eb1-111">Return value</span></span>

<span data-ttu-id="75eb1-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75eb1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75eb1-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75eb1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75eb1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="75eb1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75eb1-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="75eb1-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="75eb1-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="75eb1-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="75eb1-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="75eb1-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75eb1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75eb1-118">Requirements</span></span>



| <span data-ttu-id="75eb1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="75eb1-119">Requirement</span></span> | <span data-ttu-id="75eb1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="75eb1-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75eb1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75eb1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="75eb1-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="75eb1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75eb1-123">Library</span></span><br/> | <dl> <span data-ttu-id="75eb1-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75eb1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="75eb1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75eb1-126">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="75eb1-126">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="75eb1-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="75eb1-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




