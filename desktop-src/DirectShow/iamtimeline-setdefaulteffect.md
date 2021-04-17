---
description: O método SetDefaultEffect define o efeito padrão. Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'Método IAMTimeline:: SetDefaultEffect (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782847"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="e72c1-104">Método IAMTimeline:: SetDefaultEffect</span><span class="sxs-lookup"><span data-stu-id="e72c1-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="e72c1-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e72c1-105">\[Deprecated.</span></span> <span data-ttu-id="e72c1-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e72c1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e72c1-107">O `SetDefaultEffect` método define o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="e72c1-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="e72c1-108">Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="e72c1-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72c1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e72c1-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="e72c1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e72c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e72c1-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="e72c1-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="e72c1-112">Ponteiro para o GUID do efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="e72c1-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e72c1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e72c1-113">Return value</span></span>

<span data-ttu-id="e72c1-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e72c1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e72c1-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e72c1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e72c1-116">Remarks</span></span>

<span data-ttu-id="e72c1-117">Se você não definir um efeito padrão, ou se o efeito especificado como padrão causar um erro, o DES usará seu próprio efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="e72c1-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="e72c1-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e72c1-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e72c1-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e72c1-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e72c1-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e72c1-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e72c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e72c1-121">Requirements</span></span>



| <span data-ttu-id="e72c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e72c1-122">Requirement</span></span> | <span data-ttu-id="e72c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e72c1-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e72c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e72c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e72c1-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e72c1-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e72c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e72c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="e72c1-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e72c1-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e72c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e72c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72c1-129">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="e72c1-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e72c1-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e72c1-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




