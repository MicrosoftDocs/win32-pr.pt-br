---
description: O método InactivateWindow desativa a janela. Na classe base, esse método oculta a janela.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Método CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786998"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="ba10c-104">Método CBaseWindow. InactivateWindow</span><span class="sxs-lookup"><span data-stu-id="ba10c-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="ba10c-105">O `InactivateWindow` método desativa a janela.</span><span class="sxs-lookup"><span data-stu-id="ba10c-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="ba10c-106">Na classe base, esse método oculta a janela.</span><span class="sxs-lookup"><span data-stu-id="ba10c-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba10c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba10c-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="ba10c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba10c-108">Parameters</span></span>

<span data-ttu-id="ba10c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba10c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba10c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba10c-110">Return value</span></span>

<span data-ttu-id="ba10c-111">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba10c-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ba10c-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba10c-112">Return code</span></span>                                                                             | <span data-ttu-id="ba10c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba10c-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="ba10c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba10c-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ba10c-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ba10c-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="ba10c-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ba10c-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ba10c-117">A janela já está inativa.</span><span class="sxs-lookup"><span data-stu-id="ba10c-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ba10c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba10c-118">Requirements</span></span>



| <span data-ttu-id="ba10c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba10c-119">Requirement</span></span> | <span data-ttu-id="ba10c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ba10c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba10c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba10c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ba10c-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba10c-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba10c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba10c-123">Library</span></span><br/> | <dl> <span data-ttu-id="ba10c-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ba10c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba10c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba10c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba10c-126">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ba10c-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




