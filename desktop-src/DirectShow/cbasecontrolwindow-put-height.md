---
description: O \_ método Put Height define a altura da janela.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: Método de CBaseControlWindow.put_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755393"
---
# <a name="cbasecontrolwindowput_height-method"></a><span data-ttu-id="00b82-103">Método de altura CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="00b82-103">CBaseControlWindow.put\_Height method</span></span>

<span data-ttu-id="00b82-104">O `put_Height` método define a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="00b82-104">The `put_Height` method sets the window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00b82-105">Syntax</span></span>


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="00b82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00b82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b82-107">*Altura*</span><span class="sxs-lookup"><span data-stu-id="00b82-107">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="00b82-108">Nova altura da janela, em pixels.</span><span class="sxs-lookup"><span data-stu-id="00b82-108">New window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b82-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00b82-109">Return value</span></span>

<span data-ttu-id="00b82-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00b82-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00b82-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="00b82-111">Remarks</span></span>

<span data-ttu-id="00b82-112">A janela tem uma posição na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="00b82-112">The window has a position on the desktop.</span></span> <span data-ttu-id="00b82-113">Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior).</span><span class="sxs-lookup"><span data-stu-id="00b82-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="00b82-114">As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="00b82-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="00b82-115">Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="00b82-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="00b82-116">Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="00b82-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="00b82-117">Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.</span><span class="sxs-lookup"><span data-stu-id="00b82-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b82-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b82-118">Requirements</span></span>



| <span data-ttu-id="00b82-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b82-119">Requirement</span></span> | <span data-ttu-id="00b82-120">Valor</span><span class="sxs-lookup"><span data-stu-id="00b82-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00b82-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00b82-121">Header</span></span><br/>  | <dl> <span data-ttu-id="00b82-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00b82-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00b82-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00b82-123">Library</span></span><br/> | <dl> <span data-ttu-id="00b82-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="00b82-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b82-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="00b82-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b82-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="00b82-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




