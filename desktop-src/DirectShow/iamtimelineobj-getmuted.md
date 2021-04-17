---
description: O método getmudoed recupera o estado mudo do objeto.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'Método IAMTimelineObj:: getmudoed (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812984"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="ae56e-103">Método IAMTimelineObj:: getmudoed</span><span class="sxs-lookup"><span data-stu-id="ae56e-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="ae56e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ae56e-104">\[Deprecated.</span></span> <span data-ttu-id="ae56e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae56e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ae56e-106">O `GetMuted` método recupera o estado mudo do objeto.</span><span class="sxs-lookup"><span data-stu-id="ae56e-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae56e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae56e-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ae56e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae56e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae56e-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="ae56e-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ae56e-110">Recebe um valor que indica o estado mudo.</span><span class="sxs-lookup"><span data-stu-id="ae56e-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="ae56e-111">Se o valor for **true**, o objeto e seus filhos ficarão sem áudio.</span><span class="sxs-lookup"><span data-stu-id="ae56e-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae56e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae56e-112">Return value</span></span>

<span data-ttu-id="ae56e-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae56e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae56e-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae56e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae56e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae56e-115">Remarks</span></span>

<span data-ttu-id="ae56e-116">Se o pai de um objeto estiver mudo, o objeto ficará mudo, independentemente de seu estado mudo.</span><span class="sxs-lookup"><span data-stu-id="ae56e-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="ae56e-117">Quando o pai não estiver mais mudo, o estado anterior sem áudio do objeto será restaurado.</span><span class="sxs-lookup"><span data-stu-id="ae56e-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="ae56e-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ae56e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae56e-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae56e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ae56e-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ae56e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae56e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae56e-121">Requirements</span></span>



| <span data-ttu-id="ae56e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae56e-122">Requirement</span></span> | <span data-ttu-id="ae56e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ae56e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae56e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae56e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ae56e-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae56e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ae56e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae56e-126">Library</span></span><br/> | <dl> <span data-ttu-id="ae56e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae56e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae56e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae56e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae56e-129">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ae56e-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ae56e-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ae56e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




