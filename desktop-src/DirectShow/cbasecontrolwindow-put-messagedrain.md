---
description: O \_ método Put MessageDrain define a janela para receber mensagens de janela enviadas ao processador de vídeo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Método de CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750685"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="36208-103">Método CBaseControlWindow. put \_ MessageDrain</span><span class="sxs-lookup"><span data-stu-id="36208-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="36208-104">O `put_MessageDrain` método define a janela para receber mensagens de janela enviadas ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="36208-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="36208-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36208-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="36208-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36208-107">*Desperdício*</span><span class="sxs-lookup"><span data-stu-id="36208-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="36208-108">Janela na qual as mensagens são postadas.</span><span class="sxs-lookup"><span data-stu-id="36208-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36208-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36208-109">Return value</span></span>

<span data-ttu-id="36208-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36208-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36208-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="36208-111">Remarks</span></span>

<span data-ttu-id="36208-112">As mensagens enviadas para o filtro de processador de vídeo podem ser postadas em outra janela.</span><span class="sxs-lookup"><span data-stu-id="36208-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="36208-113">Essa função de membro registra a janela para receber essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="36208-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="36208-114">Diferentemente da função de membro [**CBaseControlWindow::p UT \_ Owner**](cbasecontrolwindow-put-owner.md) , essa função de membro não torna a janela de vídeo um filho de outra janela.</span><span class="sxs-lookup"><span data-stu-id="36208-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="36208-115">Ele é particularmente útil para renderizadores de vídeo de tela inteira, que não podem ser janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="36208-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="36208-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36208-116">Requirements</span></span>



| <span data-ttu-id="36208-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36208-117">Requirement</span></span> | <span data-ttu-id="36208-118">Valor</span><span class="sxs-lookup"><span data-stu-id="36208-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36208-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36208-119">Header</span></span><br/>  | <dl> <span data-ttu-id="36208-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36208-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36208-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36208-121">Library</span></span><br/> | <dl> <span data-ttu-id="36208-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="36208-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36208-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="36208-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36208-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="36208-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




