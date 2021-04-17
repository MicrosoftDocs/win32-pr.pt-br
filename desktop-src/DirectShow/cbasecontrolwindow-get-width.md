---
description: O \_ método obter largura recupera a largura da janela atual.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Método de CBaseControlWindow.get_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755620"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="0678d-103">Método de largura CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="0678d-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="0678d-104">O `get_Width` método recupera a largura da janela atual.</span><span class="sxs-lookup"><span data-stu-id="0678d-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="0678d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0678d-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="0678d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0678d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0678d-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="0678d-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="0678d-108">Ponteiro para a largura da janela, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0678d-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0678d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0678d-109">Return value</span></span>

<span data-ttu-id="0678d-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0678d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0678d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0678d-111">Remarks</span></span>

<span data-ttu-id="0678d-112">A janela tem uma posição na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0678d-112">The window has a position on the desktop.</span></span> <span data-ttu-id="0678d-113">Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior).</span><span class="sxs-lookup"><span data-stu-id="0678d-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="0678d-114">As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0678d-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="0678d-115">Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0678d-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="0678d-116">Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela.</span><span class="sxs-lookup"><span data-stu-id="0678d-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="0678d-117">Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.</span><span class="sxs-lookup"><span data-stu-id="0678d-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0678d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0678d-118">Requirements</span></span>



| <span data-ttu-id="0678d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0678d-119">Requirement</span></span> | <span data-ttu-id="0678d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0678d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0678d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0678d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0678d-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0678d-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0678d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0678d-123">Library</span></span><br/> | <dl> <span data-ttu-id="0678d-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0678d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0678d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0678d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0678d-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="0678d-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




