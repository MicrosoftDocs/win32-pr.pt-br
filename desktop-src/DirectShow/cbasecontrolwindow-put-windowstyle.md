---
description: O \_ método Put WindowStyle define os estilos de janela padrão.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Método de CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750684"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="d15ce-103">CBaseControlWindow. put o \_ método WindowStyle</span><span class="sxs-lookup"><span data-stu-id="d15ce-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="d15ce-104">O `put_WindowStyle` método define os estilos de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="d15ce-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d15ce-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="d15ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d15ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d15ce-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="d15ce-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="d15ce-108">Novos estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="d15ce-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d15ce-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d15ce-109">Return value</span></span>

<span data-ttu-id="d15ce-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d15ce-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d15ce-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d15ce-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15ce-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d15ce-112">Remarks</span></span>

<span data-ttu-id="d15ce-113">Tome cuidado ao alterar os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="d15ce-113">Take care when changing the window styles.</span></span> <span data-ttu-id="d15ce-114">Na maioria dos casos, um aplicativo deve recuperar o estilo atual e, em seguida, adicionar ou remover os bits inadequados.</span><span class="sxs-lookup"><span data-stu-id="d15ce-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="d15ce-115">Esse procedimento permite que vários estilos de janela internos usados pelo Windows permaneçam intactos.</span><span class="sxs-lookup"><span data-stu-id="d15ce-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="d15ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d15ce-116">Requirements</span></span>



| <span data-ttu-id="d15ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15ce-117">Requirement</span></span> | <span data-ttu-id="d15ce-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d15ce-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d15ce-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d15ce-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d15ce-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d15ce-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d15ce-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d15ce-121">Library</span></span><br/> | <dl> <span data-ttu-id="d15ce-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d15ce-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d15ce-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d15ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15ce-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="d15ce-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




