---
description: O método DoGetWindowStyle recupera os estilos de janela normais ou estendidos atuais.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909814"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="9bb8a-103">Método CBaseControlWindow. DoGetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="9bb8a-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="9bb8a-104">O `DoGetWindowStyle` método recupera os estilos de janela normal ou estendida atuais.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb8a-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="9bb8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bb8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bb8a-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="9bb8a-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="9bb8a-108">Ponteiro para uma variável que recebe as informações de estilo.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8a-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="9bb8a-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="9bb8a-110">Valor que especifica quais estilos recuperar.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="9bb8a-111">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="9bb8a-111">Must be one of the following:</span></span>



| <span data-ttu-id="9bb8a-112">Label</span><span class="sxs-lookup"><span data-stu-id="9bb8a-112">Label</span></span> | <span data-ttu-id="9bb8a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb8a-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="9bb8a-114">estilo de GWL \_</span><span class="sxs-lookup"><span data-stu-id="9bb8a-114">GWL\_STYLE</span></span>   | <span data-ttu-id="9bb8a-115">Recupere os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="9bb8a-116">GWL \_ FILEstyle</span><span class="sxs-lookup"><span data-stu-id="9bb8a-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="9bb8a-117">Recupere os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bb8a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bb8a-118">Return value</span></span>

<span data-ttu-id="9bb8a-119">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9bb8a-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb8a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bb8a-120">Remarks</span></span>

<span data-ttu-id="9bb8a-121">Essa função de membro chama a função **GetWindowLong** do Win32 para recuperar o estilo da janela.</span><span class="sxs-lookup"><span data-stu-id="9bb8a-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="9bb8a-122">Ele é chamado pelas funções membro [**CBaseControlWindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow:: get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb8a-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb8a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb8a-123">Requirements</span></span>



| <span data-ttu-id="9bb8a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bb8a-124">Requirement</span></span> | <span data-ttu-id="9bb8a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb8a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb8a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bb8a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9bb8a-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bb8a-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9bb8a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9bb8a-128">Library</span></span><br/> | <dl> <span data-ttu-id="9bb8a-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9bb8a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb8a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb8a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb8a-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="9bb8a-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




