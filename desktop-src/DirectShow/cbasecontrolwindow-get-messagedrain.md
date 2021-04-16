---
description: O \_ método Get MessageDrain recupera a mensagem atual drenagem.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Método de CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750690"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="939a1-103">CBaseControlWindow. obter \_ método MessageDrain</span><span class="sxs-lookup"><span data-stu-id="939a1-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="939a1-104">O `get_MessageDrain` método recupera a mensagem de drenagem atual.</span><span class="sxs-lookup"><span data-stu-id="939a1-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="939a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="939a1-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="939a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="939a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939a1-107">*Desperdício*</span><span class="sxs-lookup"><span data-stu-id="939a1-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="939a1-108">Ponteiro para a janela atual recebendo mensagens da janela.</span><span class="sxs-lookup"><span data-stu-id="939a1-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="939a1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="939a1-109">Return value</span></span>

<span data-ttu-id="939a1-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="939a1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="939a1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="939a1-111">Remarks</span></span>

<span data-ttu-id="939a1-112">As mensagens enviadas para o filtro de processador de vídeo podem ser postadas em outra janela.</span><span class="sxs-lookup"><span data-stu-id="939a1-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="939a1-113">A janela registrada para receber essas mensagens (usando a função de membro **CBaseControlWindow:: get \_ MessageDrain** ) é a mensagem atual drenagem.</span><span class="sxs-lookup"><span data-stu-id="939a1-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="939a1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="939a1-114">Requirements</span></span>



| <span data-ttu-id="939a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="939a1-115">Requirement</span></span> | <span data-ttu-id="939a1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="939a1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="939a1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="939a1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="939a1-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="939a1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="939a1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="939a1-119">Library</span></span><br/> | <dl> <span data-ttu-id="939a1-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="939a1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="939a1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="939a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939a1-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="939a1-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




