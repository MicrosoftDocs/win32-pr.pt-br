---
description: O método SetWindowPosition define a posição da janela na área de trabalho.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Método CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752912"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="76377-103">Método CBaseControlWindow. SetWindowPosition</span><span class="sxs-lookup"><span data-stu-id="76377-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="76377-104">O `SetWindowPosition` método define a posição da janela na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76377-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="76377-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76377-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="76377-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76377-107">*Mantida*</span><span class="sxs-lookup"><span data-stu-id="76377-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="76377-108">Nova coordenada esquerda.</span><span class="sxs-lookup"><span data-stu-id="76377-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="76377-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="76377-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="76377-110">Nova coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="76377-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="76377-111">*Largura*</span><span class="sxs-lookup"><span data-stu-id="76377-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="76377-112">Largura da janela.</span><span class="sxs-lookup"><span data-stu-id="76377-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="76377-113">*Altura*</span><span class="sxs-lookup"><span data-stu-id="76377-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="76377-114">Altura da janela.</span><span class="sxs-lookup"><span data-stu-id="76377-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76377-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76377-115">Return value</span></span>

<span data-ttu-id="76377-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76377-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76377-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76377-117">Requirements</span></span>



| <span data-ttu-id="76377-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76377-118">Requirement</span></span> | <span data-ttu-id="76377-119">Valor</span><span class="sxs-lookup"><span data-stu-id="76377-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76377-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76377-120">Header</span></span><br/>  | <dl> <span data-ttu-id="76377-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76377-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="76377-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76377-122">Library</span></span><br/> | <dl> <span data-ttu-id="76377-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="76377-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76377-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="76377-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76377-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="76377-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




