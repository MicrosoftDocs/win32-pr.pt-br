---
description: O método RemoveAll remove permanentemente esse objeto da linha do tempo, incluindo subobjetos e filhos.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'Método IAMTimelineObj:: RemoveAll (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758518"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="9a7eb-103">Método IAMTimelineObj:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="9a7eb-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="9a7eb-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-104">\[Deprecated.</span></span> <span data-ttu-id="9a7eb-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a7eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9a7eb-106">O `RemoveAll` método remove permanentemente esse objeto da linha do tempo, incluindo subobjetos e filhos.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a7eb-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="9a7eb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a7eb-108">Parameters</span></span>

<span data-ttu-id="9a7eb-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a7eb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a7eb-110">Return value</span></span>

<span data-ttu-id="9a7eb-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a7eb-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a7eb-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7eb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a7eb-113">Remarks</span></span>

<span data-ttu-id="9a7eb-114">Para remover um objeto com a finalidade de reinseri-lo em outro lugar na linha do tempo, chame [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="9a7eb-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a7eb-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9a7eb-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a7eb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9a7eb-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9a7eb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a7eb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7eb-118">Requirements</span></span>



| <span data-ttu-id="9a7eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7eb-119">Requirement</span></span> | <span data-ttu-id="9a7eb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a7eb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7eb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a7eb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9a7eb-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7eb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9a7eb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a7eb-123">Library</span></span><br/> | <dl> <span data-ttu-id="9a7eb-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a7eb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7eb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a7eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7eb-126">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="9a7eb-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9a7eb-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="9a7eb-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




