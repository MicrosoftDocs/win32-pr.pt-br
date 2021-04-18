---
description: O \_ método obter altura recupera a altura da janela atual.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Método de CBaseControlWindow.get_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752524"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="0afd1-103">Método de altura CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="0afd1-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="0afd1-104">O `get_Height` método recupera a altura da janela atual.</span><span class="sxs-lookup"><span data-stu-id="0afd1-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0afd1-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="0afd1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0afd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afd1-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="0afd1-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="0afd1-108">Ponteiro para a altura da janela atual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0afd1-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afd1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0afd1-109">Return value</span></span>

<span data-ttu-id="0afd1-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0afd1-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0afd1-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0afd1-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afd1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0afd1-112">Remarks</span></span>

<span data-ttu-id="0afd1-113">A janela tem uma posição na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0afd1-113">The window has a position on the desktop.</span></span> <span data-ttu-id="0afd1-114">Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior).</span><span class="sxs-lookup"><span data-stu-id="0afd1-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="0afd1-115">As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0afd1-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="0afd1-116">Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0afd1-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="0afd1-117">Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="0afd1-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="0afd1-118">Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.</span><span class="sxs-lookup"><span data-stu-id="0afd1-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afd1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0afd1-119">Requirements</span></span>



| <span data-ttu-id="0afd1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0afd1-120">Requirement</span></span> | <span data-ttu-id="0afd1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0afd1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afd1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0afd1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0afd1-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0afd1-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0afd1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0afd1-124">Library</span></span><br/> | <dl> <span data-ttu-id="0afd1-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0afd1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afd1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0afd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afd1-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="0afd1-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




