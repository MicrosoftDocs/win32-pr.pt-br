---
description: O \_ método Get Visible recupera a visibilidade da janela atual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Método de CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778646"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="334ca-103">CBaseControlWindow. obter \_ método visível</span><span class="sxs-lookup"><span data-stu-id="334ca-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="334ca-104">O `get_Visible` método recupera a visibilidade da janela atual.</span><span class="sxs-lookup"><span data-stu-id="334ca-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="334ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="334ca-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="334ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="334ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="334ca-107">*pVisible*</span><span class="sxs-lookup"><span data-stu-id="334ca-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="334ca-108">Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).</span><span class="sxs-lookup"><span data-stu-id="334ca-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="334ca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="334ca-109">Return value</span></span>

<span data-ttu-id="334ca-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="334ca-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="334ca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="334ca-111">Remarks</span></span>

<span data-ttu-id="334ca-112">Essa função de membro retornará 1 se a janela tiver o \_ estilo WS visível; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="334ca-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="334ca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="334ca-113">Requirements</span></span>



| <span data-ttu-id="334ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="334ca-114">Requirement</span></span> | <span data-ttu-id="334ca-115">Valor</span><span class="sxs-lookup"><span data-stu-id="334ca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="334ca-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="334ca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="334ca-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="334ca-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="334ca-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="334ca-118">Library</span></span><br/> | <dl> <span data-ttu-id="334ca-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="334ca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334ca-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="334ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334ca-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="334ca-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




