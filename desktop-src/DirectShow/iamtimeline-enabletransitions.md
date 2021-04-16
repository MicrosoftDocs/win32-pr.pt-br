---
description: O método EnableTransitions habilita ou desabilita todas as transições na linha do tempo.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Método IAMTimeline:: EnableTransitions (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752473"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="1a628-103">Método IAMTimeline:: EnableTransitions</span><span class="sxs-lookup"><span data-stu-id="1a628-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="1a628-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1a628-104">\[Deprecated.</span></span> <span data-ttu-id="1a628-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a628-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a628-106">O `EnableTransitions` método habilita ou desabilita todas as transições na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="1a628-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="1a628-107">Se as transições estiverem desabilitadas, os mecanismos de renderização as tratarão como cortes; ou seja, a saída renderizada salta instantaneamente de uma faixa para a próxima.</span><span class="sxs-lookup"><span data-stu-id="1a628-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="1a628-108">O ponto de recorte padrão é a metade da duração da transição.</span><span class="sxs-lookup"><span data-stu-id="1a628-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="1a628-109">Você pode alterar o ponto de recorte chamando o método [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) na transição.</span><span class="sxs-lookup"><span data-stu-id="1a628-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="1a628-110">As transições desabilitadas não são removidas da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="1a628-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a628-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a628-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="1a628-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a628-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a628-113">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="1a628-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="1a628-114">Valor booliano que especifica se as transições devem ser habilitadas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1a628-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="1a628-115">Se **for true**, as transições serão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="1a628-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="1a628-116">Se **for false**, as transições serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1a628-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a628-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a628-117">Return value</span></span>

<span data-ttu-id="1a628-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a628-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a628-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a628-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a628-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a628-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a628-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1a628-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a628-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a628-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a628-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a628-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a628-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a628-124">Requirements</span></span>



| <span data-ttu-id="1a628-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a628-125">Requirement</span></span> | <span data-ttu-id="1a628-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1a628-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a628-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a628-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1a628-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a628-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a628-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a628-129">Library</span></span><br/> | <dl> <span data-ttu-id="1a628-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a628-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a628-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a628-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a628-132">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="1a628-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="1a628-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1a628-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




