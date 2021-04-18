---
description: O \_ método Put alfa Especifica o valor alfa para a imagem inteira.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: método de ut_Alpha de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758838"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="911e4-103">Método IDxtAlphaSetter::p UT \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="911e4-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="911e4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="911e4-104">\[Deprecated.</span></span> <span data-ttu-id="911e4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="911e4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="911e4-106">O `put_Alpha` método especifica o valor alfa para a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="911e4-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="911e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="911e4-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="911e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="911e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="911e4-109">*Alfa* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="911e4-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911e4-110">O valor alfa.</span><span class="sxs-lookup"><span data-stu-id="911e4-110">The alpha value.</span></span> <span data-ttu-id="911e4-111">Esse valor será aplicado a toda a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="911e4-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="911e4-112">Para desabilitar essa propriedade, defina um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="911e4-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="911e4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="911e4-113">Return value</span></span>

<span data-ttu-id="911e4-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="911e4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="911e4-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="911e4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="911e4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="911e4-116">Remarks</span></span>

<span data-ttu-id="911e4-117">Se você definir essa propriedade como um valor não negativo, também deverá desabilitar a propriedade de rampa alfa chamando **Put \_ AlphaRamp** com um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="911e4-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="911e4-118">Caso contrário, o efeito não será renderizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="911e4-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="911e4-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="911e4-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="911e4-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="911e4-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="911e4-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="911e4-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="911e4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="911e4-122">Requirements</span></span>



| <span data-ttu-id="911e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="911e4-123">Requirement</span></span> | <span data-ttu-id="911e4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="911e4-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="911e4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="911e4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="911e4-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="911e4-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="911e4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="911e4-127">Library</span></span><br/> | <dl> <span data-ttu-id="911e4-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="911e4-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="911e4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="911e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="911e4-130">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="911e4-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="911e4-131">**IDxtAlphaSetter::p UT \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="911e4-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




