---
description: O método SetSwapInputs especifica se as entradas de transição são trocadas.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Método IAMTimelineTrans:: SetSwapInputs (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779845"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="c7353-103">Método IAMTimelineTrans:: SetSwapInputs</span><span class="sxs-lookup"><span data-stu-id="c7353-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="c7353-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c7353-104">\[Deprecated.</span></span> <span data-ttu-id="c7353-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7353-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7353-106">O `SetSwapInputs` método especifica se as entradas de transição são trocadas.</span><span class="sxs-lookup"><span data-stu-id="c7353-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="c7353-107">Por padrão, uma transição é proveniente da composição de todas as camadas de prioridade inferior para a camada em que reside a transição.</span><span class="sxs-lookup"><span data-stu-id="c7353-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="c7353-108">Você pode reverter essa progressão, de modo que a transição vai da camada onde ela reside de volta para a composição de camadas de prioridade inferior.</span><span class="sxs-lookup"><span data-stu-id="c7353-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="c7353-109">Para obter mais informações, consulte [direção da transição](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="c7353-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7353-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7353-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="c7353-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7353-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7353-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="c7353-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="c7353-113">Especifica se as entradas são trocadas.</span><span class="sxs-lookup"><span data-stu-id="c7353-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="c7353-114">Se **for false**, a transição passará da composição de todas as camadas de prioridade inferior para a camada de transição.</span><span class="sxs-lookup"><span data-stu-id="c7353-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="c7353-115">Se **for true**, a transição vai para a direção oposta.</span><span class="sxs-lookup"><span data-stu-id="c7353-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7353-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7353-116">Return value</span></span>

<span data-ttu-id="c7353-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c7353-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7353-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7353-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7353-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7353-119">Remarks</span></span>

<span data-ttu-id="c7353-120">Esse método não altera a direção do efeito visual.</span><span class="sxs-lookup"><span data-stu-id="c7353-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="c7353-121">Por exemplo, um apagamento da esquerda para a direita ainda passará da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="c7353-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="c7353-122">Para alterar a direção, defina a propriedade **Progress** usando a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="c7353-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="c7353-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c7353-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7353-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7353-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7353-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c7353-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7353-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7353-126">Requirements</span></span>



| <span data-ttu-id="c7353-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7353-127">Requirement</span></span> | <span data-ttu-id="c7353-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c7353-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7353-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7353-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c7353-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7353-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7353-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7353-131">Library</span></span><br/> | <dl> <span data-ttu-id="c7353-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7353-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7353-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7353-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7353-134">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="c7353-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="c7353-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c7353-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




