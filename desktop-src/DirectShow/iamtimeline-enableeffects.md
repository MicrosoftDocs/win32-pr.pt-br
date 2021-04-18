---
description: O método EnableEffects habilita ou desabilita todos os efeitos na linha do tempo. Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Método IAMTimeline:: EnableEffects (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766308"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="980bb-104">Método IAMTimeline:: EnableEffects</span><span class="sxs-lookup"><span data-stu-id="980bb-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="980bb-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="980bb-105">\[Deprecated.</span></span> <span data-ttu-id="980bb-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="980bb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="980bb-107">O `EnableEffects` método habilita ou desabilita todos os efeitos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="980bb-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="980bb-108">Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.</span><span class="sxs-lookup"><span data-stu-id="980bb-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="980bb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="980bb-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="980bb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="980bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="980bb-111">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="980bb-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="980bb-112">Valor booliano que especifica se os efeitos devem ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="980bb-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="980bb-113">Se **for true**, os efeitos serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="980bb-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="980bb-114">Se **for false**, os efeitos serão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="980bb-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="980bb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="980bb-115">Return value</span></span>

<span data-ttu-id="980bb-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="980bb-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="980bb-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="980bb-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="980bb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="980bb-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="980bb-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="980bb-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="980bb-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="980bb-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="980bb-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="980bb-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="980bb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="980bb-122">Requirements</span></span>



| <span data-ttu-id="980bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="980bb-123">Requirement</span></span> | <span data-ttu-id="980bb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="980bb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="980bb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="980bb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="980bb-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="980bb-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="980bb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="980bb-127">Library</span></span><br/> | <dl> <span data-ttu-id="980bb-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="980bb-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="980bb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="980bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980bb-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="980bb-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="980bb-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="980bb-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




