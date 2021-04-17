---
description: O método InitialiseWindow Inicializa a janela.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812853"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="8ba52-103">CBaseWindow.Inimétodo tialiseWindow</span><span class="sxs-lookup"><span data-stu-id="8ba52-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="8ba52-104">O `InitialiseWindow` método inicializa a janela.</span><span class="sxs-lookup"><span data-stu-id="8ba52-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ba52-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="8ba52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ba52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba52-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8ba52-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba52-108">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="8ba52-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba52-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ba52-109">Return value</span></span>

<span data-ttu-id="8ba52-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ba52-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba52-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ba52-111">Remarks</span></span>

<span data-ttu-id="8ba52-112">Por padrão, esse método recupera um identificador para o contexto de dispositivo (DC) da janela e cria um controlador de domínio de memória compatível.</span><span class="sxs-lookup"><span data-stu-id="8ba52-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="8ba52-113">No entanto, se o valor do sinalizador [**CBaseWindow:: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) for **false**, esse método não recuperará os contextos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ba52-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="8ba52-114">O DC de memória é útil para selecionar bitmaps antes de blittable para a janela.</span><span class="sxs-lookup"><span data-stu-id="8ba52-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="8ba52-115">O método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="8ba52-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba52-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba52-116">Requirements</span></span>



| <span data-ttu-id="8ba52-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba52-117">Requirement</span></span> | <span data-ttu-id="8ba52-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8ba52-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba52-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ba52-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba52-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba52-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ba52-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ba52-121">Library</span></span><br/> | <dl> <span data-ttu-id="8ba52-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba52-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba52-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ba52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba52-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="8ba52-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




