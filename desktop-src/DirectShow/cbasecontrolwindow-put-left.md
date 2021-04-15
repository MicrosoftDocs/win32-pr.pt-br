---
description: O \_ método Put Left define a coordenada esquerda para a janela.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Método de CBaseControlWindow.put_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753754"
---
# <a name="cbasecontrolwindowput_left-method"></a><span data-ttu-id="fec3c-103">Método CBaseControlWindow. put \_ esquerdo</span><span class="sxs-lookup"><span data-stu-id="fec3c-103">CBaseControlWindow.put\_Left method</span></span>

<span data-ttu-id="fec3c-104">O `put_Left` método define a coordenada esquerda para a janela.</span><span class="sxs-lookup"><span data-stu-id="fec3c-104">The `put_Left` method sets the left coordinate for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec3c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fec3c-105">Syntax</span></span>


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a><span data-ttu-id="fec3c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fec3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec3c-107">*Mantida*</span><span class="sxs-lookup"><span data-stu-id="fec3c-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="fec3c-108">Nova coordenada esquerda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="fec3c-108">New left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec3c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fec3c-109">Return value</span></span>

<span data-ttu-id="fec3c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fec3c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec3c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fec3c-111">Remarks</span></span>

<span data-ttu-id="fec3c-112">A janela tem uma posição na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fec3c-112">The window has a position on the desktop.</span></span> <span data-ttu-id="fec3c-113">Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior).</span><span class="sxs-lookup"><span data-stu-id="fec3c-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="fec3c-114">As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fec3c-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="fec3c-115">Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="fec3c-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="fec3c-116">Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="fec3c-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="fec3c-117">Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.</span><span class="sxs-lookup"><span data-stu-id="fec3c-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec3c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec3c-118">Requirements</span></span>



| <span data-ttu-id="fec3c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec3c-119">Requirement</span></span> | <span data-ttu-id="fec3c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fec3c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec3c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fec3c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fec3c-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fec3c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fec3c-123">Library</span></span><br/> | <dl> <span data-ttu-id="fec3c-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec3c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec3c-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="fec3c-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




