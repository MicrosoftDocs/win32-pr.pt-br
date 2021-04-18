---
description: O método SetCutsOnly especifica se a transição é renderizada como um recorte. Nesse caso, a transição ocorre instantaneamente no ponto de recorte. Se uma transição levar muito tempo para ser renderizada, talvez você queira visualizá-la como uma visualização de velocidade de recortar.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Método IAMTimelineTrans:: SetCutsOnly (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782840"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="dd30b-105">Método IAMTimelineTrans:: SetCutsOnly</span><span class="sxs-lookup"><span data-stu-id="dd30b-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="dd30b-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="dd30b-106">\[Deprecated.</span></span> <span data-ttu-id="dd30b-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd30b-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dd30b-108">O `SetCutsOnly` método especifica se a transição é renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="dd30b-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="dd30b-109">Nesse caso, a transição ocorre instantaneamente no ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="dd30b-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="dd30b-110">Se uma transição levar muito tempo para ser renderizada, talvez você queira visualizá-la como uma visualização de velocidade de recortar.</span><span class="sxs-lookup"><span data-stu-id="dd30b-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd30b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd30b-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="dd30b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd30b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd30b-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="dd30b-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="dd30b-114">Especifica se a transição deve ser renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="dd30b-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="dd30b-115">Se for **true**, a transição será renderizada como uma recorte instantânea.</span><span class="sxs-lookup"><span data-stu-id="dd30b-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="dd30b-116">Se **for false**, a transição renderizará ao longo de sua duração normal.</span><span class="sxs-lookup"><span data-stu-id="dd30b-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd30b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd30b-117">Return value</span></span>

<span data-ttu-id="dd30b-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd30b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd30b-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd30b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd30b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd30b-120">Remarks</span></span>

<span data-ttu-id="dd30b-121">A renderização de uma transição como um recorte não é compatível com a troca de entradas.</span><span class="sxs-lookup"><span data-stu-id="dd30b-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="dd30b-122">(Consulte [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Se você chamar `SetCutsOnly` com um valor de **true**, ele substituirá temporariamente a configuração **SetSwapInputs** .</span><span class="sxs-lookup"><span data-stu-id="dd30b-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="dd30b-123">No entanto, a configuração somente de recorte é destinada à visualização, portanto, essa limitação não afeta a saída do arquivo, apenas lembre-se de chamar `SetCutsOnly` com o valor **false** antes de gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd30b-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="dd30b-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="dd30b-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dd30b-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd30b-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dd30b-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dd30b-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd30b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd30b-127">Requirements</span></span>



| <span data-ttu-id="dd30b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd30b-128">Requirement</span></span> | <span data-ttu-id="dd30b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dd30b-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd30b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd30b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dd30b-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd30b-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dd30b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd30b-132">Library</span></span><br/> | <dl> <span data-ttu-id="dd30b-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd30b-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd30b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd30b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd30b-135">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="dd30b-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="dd30b-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="dd30b-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




