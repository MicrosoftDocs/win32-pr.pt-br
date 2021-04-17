---
description: O \_ método Put janelastate define o estado da janela.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Método de CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749854"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="c1632-103">Método WindowState de CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="c1632-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="c1632-104">O `put_WindowState` método define o estado da janela.</span><span class="sxs-lookup"><span data-stu-id="c1632-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1632-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1632-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="c1632-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1632-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="c1632-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="c1632-108">Novo estado da janela.</span><span class="sxs-lookup"><span data-stu-id="c1632-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1632-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1632-109">Return value</span></span>

<span data-ttu-id="c1632-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1632-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1632-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1632-111">Remarks</span></span>

<span data-ttu-id="c1632-112">Essa função de membro usa os mesmos parâmetros que a função Microsoft Win32 **userwindow** (por exemplo, WS- \_ normal, WS \_ SHOWMINNOACTIVATE e WS não \_ Maximized).</span><span class="sxs-lookup"><span data-stu-id="c1632-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1632-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1632-113">Requirements</span></span>



| <span data-ttu-id="c1632-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1632-114">Requirement</span></span> | <span data-ttu-id="c1632-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c1632-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1632-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1632-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c1632-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1632-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1632-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1632-118">Library</span></span><br/> | <dl> <span data-ttu-id="c1632-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c1632-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1632-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1632-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1632-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="c1632-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




