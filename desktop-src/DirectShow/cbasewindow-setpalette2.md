---
description: O método SetPalette instala uma paleta para a janela. Esse método não tem parâmetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Método CBaseWindow. SetPalette (Winutil. h)-sem parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104173218"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="ebb83-104">Método CBaseWindow. SetPalette (Winutil. h)-sem parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebb83-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="ebb83-105">O `SetPalette` método instala uma paleta para a janela.</span><span class="sxs-lookup"><span data-stu-id="ebb83-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb83-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebb83-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="ebb83-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebb83-107">Parameters</span></span>

<span data-ttu-id="ebb83-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ebb83-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebb83-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebb83-109">Return value</span></span>

<span data-ttu-id="ebb83-110">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ebb83-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ebb83-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ebb83-111">Return code</span></span>                                                                             | <span data-ttu-id="ebb83-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebb83-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="ebb83-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ebb83-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ebb83-114">Uma chamada interna para **GdiFlush** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="ebb83-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="ebb83-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebb83-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ebb83-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ebb83-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ebb83-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebb83-117">Remarks</span></span>

<span data-ttu-id="ebb83-118">A paleta fornecida pela variável de membro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) é selecionada.</span><span class="sxs-lookup"><span data-stu-id="ebb83-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="ebb83-119">O chamador deve garantir a validade de **m \_ hPalette**.</span><span class="sxs-lookup"><span data-stu-id="ebb83-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="ebb83-120">Se o valor da variável de membro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) for **false** (o padrão), esse método selecionará a paleta e a perceberá.</span><span class="sxs-lookup"><span data-stu-id="ebb83-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="ebb83-121">Caso contrário, ele seleciona a paleta, mas não a percebe.</span><span class="sxs-lookup"><span data-stu-id="ebb83-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="ebb83-122">O objeto não exclui nenhuma paleta anterior que estava sendo usada.</span><span class="sxs-lookup"><span data-stu-id="ebb83-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="ebb83-123">O chamador é responsável por excluir paletas.</span><span class="sxs-lookup"><span data-stu-id="ebb83-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="ebb83-124">Qualquer thread pode chamar esse método com segurança, não apenas o thread que possui a janela.</span><span class="sxs-lookup"><span data-stu-id="ebb83-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="ebb83-125">A janela envia uma mensagem particular para si mesma, que dispara uma chamada para o método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb83-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb83-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb83-126">Requirements</span></span>

| <span data-ttu-id="ebb83-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb83-127">Requirement</span></span> | <span data-ttu-id="ebb83-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ebb83-128">Value</span></span> |
|-|-|
| <span data-ttu-id="ebb83-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebb83-129">Header</span></span> | <span data-ttu-id="ebb83-130">Winutil. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="ebb83-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="ebb83-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebb83-131">Library</span></span>| <span data-ttu-id="ebb83-132">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="ebb83-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ebb83-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebb83-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb83-134">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ebb83-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




