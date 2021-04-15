---
description: O \_ método Get AlphaRamp recupera a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Método IDxtAlphaSetter:: get_AlphaRamp (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760878"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="d2b2b-105">Método IDxtAlphaSetter:: get \_ AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="d2b2b-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="d2b2b-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-106">\[Deprecated.</span></span> <span data-ttu-id="d2b2b-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2b2b-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2b2b-108">O `get_AlphaRamp` método recupera a propriedade de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="d2b2b-109">A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="d2b2b-110">Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b2b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2b2b-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="d2b2b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2b2b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b2b-113">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d2b2b-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b2b-114">Recebe a rampa de alfa.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-114">Receives the alpha ramp.</span></span> <span data-ttu-id="d2b2b-115">Um valor negativo indica que nenhuma rampa de alfa está definida.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b2b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2b2b-116">Return value</span></span>

<span data-ttu-id="d2b2b-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2b2b-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d2b2b-118">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-118">Possible values include the following.</span></span>



| <span data-ttu-id="d2b2b-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d2b2b-119">Return code</span></span>                                                                               | <span data-ttu-id="d2b2b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2b2b-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d2b2b-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b2b-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d2b2b-122">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="d2b2b-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="d2b2b-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b2b-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d2b2b-124">Sucesso</span><span class="sxs-lookup"><span data-stu-id="d2b2b-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d2b2b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2b2b-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2b2b-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2b2b-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2b2b-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2b2b-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d2b2b-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2b2b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2b2b-129">Requirements</span></span>



| <span data-ttu-id="d2b2b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2b2b-130">Requirement</span></span> | <span data-ttu-id="d2b2b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d2b2b-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b2b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2b2b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d2b2b-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b2b-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2b2b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2b2b-134">Library</span></span><br/> | <dl> <span data-ttu-id="d2b2b-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2b2b-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b2b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2b2b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b2b-137">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="d2b2b-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




