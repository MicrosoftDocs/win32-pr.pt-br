---
description: O \_ método Get WindowState recupera o estado da janela atual.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Método de CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754568"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="ccd43-103">Método WindowState de CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="ccd43-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="ccd43-104">O `get_WindowState` método recupera o estado da janela atual.</span><span class="sxs-lookup"><span data-stu-id="ccd43-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd43-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="ccd43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd43-107">*pWindowState*</span><span class="sxs-lookup"><span data-stu-id="ccd43-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd43-108">Ponteiro para o estado da janela.</span><span class="sxs-lookup"><span data-stu-id="ccd43-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd43-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccd43-109">Return value</span></span>

<span data-ttu-id="ccd43-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccd43-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd43-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccd43-111">Remarks</span></span>

<span data-ttu-id="ccd43-112">Essa função de membro retorna um subconjunto dos parâmetros da função Microsoft Win32 **userwindow** .</span><span class="sxs-lookup"><span data-stu-id="ccd43-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="ccd43-113">Em particular, ele retorna \_ o SW show e o SW \_ Hide, dependendo da visibilidade atual da janela.</span><span class="sxs-lookup"><span data-stu-id="ccd43-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="ccd43-114">Ele também retorna \_ a minimização de SW e \_ o SW maximizar, dependendo se a janela é um ícone ou é expandida.</span><span class="sxs-lookup"><span data-stu-id="ccd43-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd43-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd43-115">Requirements</span></span>



| <span data-ttu-id="ccd43-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd43-116">Requirement</span></span> | <span data-ttu-id="ccd43-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd43-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd43-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccd43-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ccd43-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccd43-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ccd43-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccd43-120">Library</span></span><br/> | <dl> <span data-ttu-id="ccd43-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ccd43-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd43-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccd43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd43-123">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="ccd43-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




