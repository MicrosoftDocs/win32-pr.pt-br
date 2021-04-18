---
description: O método remove remove esse objeto da linha do tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Método IAMTimelineObj:: Remove (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761762"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="51b3e-103">Método IAMTimelineObj:: Remove</span><span class="sxs-lookup"><span data-stu-id="51b3e-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="51b3e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="51b3e-104">\[Deprecated.</span></span> <span data-ttu-id="51b3e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51b3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51b3e-106">O `Remove` método remove esse objeto da linha do tempo (incluindo subobjetos, mas não filhos), para reinserção em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="51b3e-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51b3e-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="51b3e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51b3e-108">Parameters</span></span>

<span data-ttu-id="51b3e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51b3e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51b3e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51b3e-110">Return value</span></span>

<span data-ttu-id="51b3e-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="51b3e-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51b3e-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51b3e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b3e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="51b3e-113">Remarks</span></span>

<span data-ttu-id="51b3e-114">Chame esse método somente se o aplicativo inserir imediatamente o objeto de volta na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="51b3e-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="51b3e-115">É uma operação inválida para chamar esse método sem, em seguida, reinserir o objeto.</span><span class="sxs-lookup"><span data-stu-id="51b3e-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="51b3e-116">Para remover um objeto permanentemente, chame [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="51b3e-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="51b3e-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="51b3e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="51b3e-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51b3e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="51b3e-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="51b3e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51b3e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51b3e-120">Requirements</span></span>



| <span data-ttu-id="51b3e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b3e-121">Requirement</span></span> | <span data-ttu-id="51b3e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="51b3e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51b3e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51b3e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="51b3e-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b3e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="51b3e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51b3e-125">Library</span></span><br/> | <dl> <span data-ttu-id="51b3e-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51b3e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b3e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="51b3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b3e-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="51b3e-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="51b3e-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="51b3e-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




