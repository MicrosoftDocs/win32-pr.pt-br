---
description: O \_ método Get Left recupera a coordenada da janela esquerda atual.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Método de CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756648"
---
# <a name="cbasecontrolwindowget_left-method"></a><span data-ttu-id="9df4f-103">Método Left de CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="9df4f-103">CBaseControlWindow.get\_Left method</span></span>

<span data-ttu-id="9df4f-104">O `get_Left` método recupera a coordenada da janela esquerda atual.</span><span class="sxs-lookup"><span data-stu-id="9df4f-104">The `get_Left` method retrieves the current left window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9df4f-105">Syntax</span></span>


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a><span data-ttu-id="9df4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9df4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df4f-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="9df4f-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="9df4f-108">Ponteiro para a coordenada esquerda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9df4f-108">Pointer to the left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df4f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9df4f-109">Return value</span></span>

<span data-ttu-id="9df4f-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9df4f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df4f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9df4f-111">Remarks</span></span>

<span data-ttu-id="9df4f-112">A janela tem uma posição na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9df4f-112">The window has a position on the desktop.</span></span> <span data-ttu-id="9df4f-113">Essa posição é expressa em pixels por quatro coordenadas (esquerda, superior, direita e inferior).</span><span class="sxs-lookup"><span data-stu-id="9df4f-113">This position is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="9df4f-114">As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9df4f-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="9df4f-115">Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9df4f-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="9df4f-116">Definir as coordenadas esquerda ou superior move a janela para a esquerda e para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="9df4f-116">Setting the left or top coordinates moves the window left and up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="9df4f-117">Da mesma forma, definir a largura e a altura não tem efeito nas coordenadas esquerda e superior.</span><span class="sxs-lookup"><span data-stu-id="9df4f-117">Likewise, setting the width and height have no effect on the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df4f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9df4f-118">Requirements</span></span>



| <span data-ttu-id="9df4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df4f-119">Requirement</span></span> | <span data-ttu-id="9df4f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9df4f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df4f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9df4f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9df4f-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9df4f-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9df4f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9df4f-123">Library</span></span><br/> | <dl> <span data-ttu-id="9df4f-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9df4f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df4f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9df4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df4f-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="9df4f-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




