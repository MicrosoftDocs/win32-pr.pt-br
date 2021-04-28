---
description: Construtor de CBaseWindow. CBaseWindow-método de construtor.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Construtor CBaseWindow. CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095814"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="704fa-103">Construtor CBaseWindow. CBaseWindow</span><span class="sxs-lookup"><span data-stu-id="704fa-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="704fa-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="704fa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="704fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="704fa-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="704fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="704fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="704fa-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="704fa-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="704fa-108">Valor booliano que especifica se o contexto do dispositivo deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="704fa-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="704fa-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="704fa-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="704fa-110">Valor booliano que especifica a variável de membro [**CBaseWindow:: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .</span><span class="sxs-lookup"><span data-stu-id="704fa-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="704fa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="704fa-111">Remarks</span></span>

<span data-ttu-id="704fa-112">Depois de criar o objeto, chame o método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) para criar a janela.</span><span class="sxs-lookup"><span data-stu-id="704fa-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="704fa-113">**PrepareWindow** é um método virtual.</span><span class="sxs-lookup"><span data-stu-id="704fa-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="704fa-114">Ele chama [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md), também um método virtual.</span><span class="sxs-lookup"><span data-stu-id="704fa-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="704fa-115">Esses métodos são separados do construtor para que as classes derivadas possam substituí-los, se necessário.</span><span class="sxs-lookup"><span data-stu-id="704fa-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="704fa-116">Se o valor do parâmetro *bDoGetDC* for **true**, o `CBaseWindow` objeto recuperará um identificador para o DC (contexto de dispositivo) da janela e o armazenará na variável de membro [**\_ HDC CBaseWindow:: m**](cbasewindow-m-hdc.md) .</span><span class="sxs-lookup"><span data-stu-id="704fa-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="704fa-117">O objeto também cria um controlador de domínio de memória compatível, que ele armazena na variável de membro [**CBaseWindow:: m \_ MemoryDC**](cbasewindow-m-memorydc.md) .</span><span class="sxs-lookup"><span data-stu-id="704fa-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="704fa-118">Essas ações ocorrem no método **InitialiseWindow** .</span><span class="sxs-lookup"><span data-stu-id="704fa-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="704fa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704fa-119">Requirements</span></span>



| <span data-ttu-id="704fa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="704fa-120">Requirement</span></span> | <span data-ttu-id="704fa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="704fa-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="704fa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="704fa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="704fa-123"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="704fa-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="704fa-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="704fa-124">Library</span></span><br/> | <dl> <span data-ttu-id="704fa-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="704fa-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704fa-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="704fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704fa-127">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="704fa-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




