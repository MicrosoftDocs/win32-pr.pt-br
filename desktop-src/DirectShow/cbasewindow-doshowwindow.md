---
description: O método DoShowWindow define o estado de exibição da janela.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Método CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758699"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="4ccbe-103">Método CBaseWindow. DoShowWindow</span><span class="sxs-lookup"><span data-stu-id="4ccbe-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="4ccbe-104">O método **DoShowWindow** define o estado de exibição da janela.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ccbe-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="4ccbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ccbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccbe-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="4ccbe-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="4ccbe-108">Sinalizador que especifica como a janela deve ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="4ccbe-109">O valor pode ser qualquer constante definida para o parâmetro *nCmdShow* da função de [**janela**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="4ccbe-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccbe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ccbe-110">Return value</span></span>

<span data-ttu-id="4ccbe-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ccbe-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ccbe-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ccbe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ccbe-113">Requirements</span></span>



| <span data-ttu-id="4ccbe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ccbe-114">Requirement</span></span> | <span data-ttu-id="4ccbe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4ccbe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccbe-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ccbe-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4ccbe-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ccbe-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ccbe-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ccbe-118">Library</span></span><br/> | <dl> <span data-ttu-id="4ccbe-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4ccbe-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ccbe-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ccbe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccbe-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="4ccbe-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

