---
description: O método SetPalette instala uma paleta para a janela.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Método CBaseWindow. SetPalette (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752706"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="5f1e2-103">Método CBaseWindow. SetPalette (Winutil. h)</span><span class="sxs-lookup"><span data-stu-id="5f1e2-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="5f1e2-104">O `SetPalette` método instala uma paleta para a janela.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f1e2-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="5f1e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f1e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1e2-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="5f1e2-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="5f1e2-108">Identificador para a nova paleta.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-108">Handle to the new palette.</span></span> <span data-ttu-id="5f1e2-109">Não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1e2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f1e2-110">Return value</span></span>

<span data-ttu-id="5f1e2-111">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5f1e2-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f1e2-112">Return code</span></span>                                                                             | <span data-ttu-id="5f1e2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f1e2-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="5f1e2-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1e2-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5f1e2-115">Uma chamada interna para **GdiFlush** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="5f1e2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1e2-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5f1e2-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="5f1e2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f1e2-118">Remarks</span></span>

<span data-ttu-id="5f1e2-119">Se o valor da variável de membro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) for **false** (o padrão), esse método selecionará a paleta e a perceberá.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="5f1e2-120">Caso contrário, ele seleciona a paleta, mas não a percebe.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="5f1e2-121">O objeto não exclui nenhuma paleta anterior que estava sendo usada.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="5f1e2-122">O chamador é responsável por excluir paletas.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="5f1e2-123">Qualquer thread pode chamar esse método com segurança, não apenas o thread que possui a janela.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="5f1e2-124">A janela envia uma mensagem particular para si mesma, que dispara uma chamada para o método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1e2-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1e2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f1e2-125">Requirements</span></span>



| <span data-ttu-id="5f1e2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1e2-126">Requirement</span></span> | <span data-ttu-id="5f1e2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5f1e2-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1e2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f1e2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5f1e2-129"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f1e2-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f1e2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f1e2-130">Library</span></span><br/> | <dl> <span data-ttu-id="5f1e2-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f1e2-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f1e2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f1e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1e2-133">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




