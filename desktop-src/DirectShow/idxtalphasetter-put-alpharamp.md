---
description: O \_ método Put AlphaRamp especifica a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: método de ut_AlphaRamp de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758056"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="81023-105">IDxtAlphaSetter: método UT \_ AlphaRamp:p</span><span class="sxs-lookup"><span data-stu-id="81023-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="81023-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="81023-106">\[Deprecated.</span></span> <span data-ttu-id="81023-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81023-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81023-108">O `put_AlphaRamp` método especifica a propriedade de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="81023-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="81023-109">A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados.</span><span class="sxs-lookup"><span data-stu-id="81023-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="81023-110">Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.</span><span class="sxs-lookup"><span data-stu-id="81023-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="81023-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81023-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="81023-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81023-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81023-113">*Alfa* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81023-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81023-114">A rampa alfa como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="81023-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="81023-115">Por exemplo, 1,0 é 100%.</span><span class="sxs-lookup"><span data-stu-id="81023-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="81023-116">Para desabilitar essa propriedade, defina um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="81023-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81023-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81023-117">Return value</span></span>

<span data-ttu-id="81023-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81023-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81023-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81023-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81023-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="81023-120">Remarks</span></span>

<span data-ttu-id="81023-121">Se você definir essa propriedade como um valor não negativo, também deverá desabilitar a propriedade Alpha chamando **Put \_ alfa** com um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="81023-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="81023-122">Caso contrário, o efeito não será renderizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="81023-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="81023-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="81023-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81023-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81023-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81023-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81023-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81023-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81023-126">Requirements</span></span>



| <span data-ttu-id="81023-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="81023-127">Requirement</span></span> | <span data-ttu-id="81023-128">Valor</span><span class="sxs-lookup"><span data-stu-id="81023-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81023-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81023-129">Header</span></span><br/>  | <dl> <span data-ttu-id="81023-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81023-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81023-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81023-131">Library</span></span><br/> | <dl> <span data-ttu-id="81023-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81023-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81023-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="81023-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81023-134">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="81023-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="81023-135">**IDxtAlphaSetter::p UT \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="81023-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




