---
description: O \_ método Get Alpha recupera o valor alfa de toda a imagem.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Método IDxtAlphaSetter:: get_Alpha (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782839"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="2ce1e-103">Método IDxtAlphaSetter:: get \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="2ce1e-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="2ce1e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-104">\[Deprecated.</span></span> <span data-ttu-id="2ce1e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ce1e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2ce1e-106">O `get_Alpha` método recupera o valor alfa para a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce1e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ce1e-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="2ce1e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ce1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce1e-109">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2ce1e-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce1e-110">Recebe o valor alfa.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-110">Receives the alpha value.</span></span> <span data-ttu-id="2ce1e-111">Esse valor alfa será aplicado à imagem de destino inteira.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="2ce1e-112">Um valor negativo indica que nenhum valor alfa está definido.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce1e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ce1e-113">Return value</span></span>

<span data-ttu-id="2ce1e-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ce1e-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2ce1e-115">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-115">Possible values include the following.</span></span>



| <span data-ttu-id="2ce1e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2ce1e-116">Return code</span></span>                                                                               | <span data-ttu-id="2ce1e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ce1e-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="2ce1e-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1e-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2ce1e-119">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="2ce1e-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="2ce1e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1e-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2ce1e-121">Sucesso</span><span class="sxs-lookup"><span data-stu-id="2ce1e-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="2ce1e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ce1e-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ce1e-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2ce1e-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2ce1e-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2ce1e-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2ce1e-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ce1e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ce1e-126">Requirements</span></span>



| <span data-ttu-id="2ce1e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce1e-127">Requirement</span></span> | <span data-ttu-id="2ce1e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2ce1e-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce1e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ce1e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce1e-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1e-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2ce1e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ce1e-131">Library</span></span><br/> | <dl> <span data-ttu-id="2ce1e-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1e-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce1e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ce1e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce1e-134">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="2ce1e-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




