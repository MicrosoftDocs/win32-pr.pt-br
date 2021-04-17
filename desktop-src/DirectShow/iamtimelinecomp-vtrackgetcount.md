---
description: O método VTrackGetCount recupera o número de faixas virtuais contidas na composição.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'Método IAMTimelineComp:: VTrackGetCount (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812986"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="cc620-103">Método IAMTimelineComp:: VTrackGetCount</span><span class="sxs-lookup"><span data-stu-id="cc620-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="cc620-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="cc620-104">\[Deprecated.</span></span> <span data-ttu-id="cc620-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc620-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc620-106">O `VTrackGetCount` método recupera o número de faixas virtuais contidas na composição.</span><span class="sxs-lookup"><span data-stu-id="cc620-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc620-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc620-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cc620-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc620-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc620-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="cc620-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="cc620-110">Recebe o número de faixas virtuais.</span><span class="sxs-lookup"><span data-stu-id="cc620-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc620-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc620-111">Return value</span></span>

<span data-ttu-id="cc620-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc620-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc620-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc620-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc620-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc620-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc620-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="cc620-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc620-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc620-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc620-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cc620-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc620-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc620-118">Requirements</span></span>



| <span data-ttu-id="cc620-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc620-119">Requirement</span></span> | <span data-ttu-id="cc620-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cc620-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc620-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc620-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cc620-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc620-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc620-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc620-123">Library</span></span><br/> | <dl> <span data-ttu-id="cc620-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc620-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc620-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc620-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc620-126">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="cc620-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="cc620-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="cc620-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




