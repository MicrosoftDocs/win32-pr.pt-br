---
description: O método HideCursor oculta ou exibe o cursor.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Método CBaseControlWindow. HideCursor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750077"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="b080e-103">Método CBaseControlWindow. HideCursor</span><span class="sxs-lookup"><span data-stu-id="b080e-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="b080e-104">O `HideCursor` método oculta ou exibe o cursor.</span><span class="sxs-lookup"><span data-stu-id="b080e-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b080e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b080e-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="b080e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b080e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b080e-107">*HideCursor*</span><span class="sxs-lookup"><span data-stu-id="b080e-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="b080e-108">Valor que especifica se o cursor deve ser mostrado.</span><span class="sxs-lookup"><span data-stu-id="b080e-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="b080e-109">Defina como OATRUE para ocultar o cursor ou OAFALSE para exibir o cursor.</span><span class="sxs-lookup"><span data-stu-id="b080e-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b080e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b080e-110">Return value</span></span>

<span data-ttu-id="b080e-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b080e-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b080e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b080e-112">Requirements</span></span>



| <span data-ttu-id="b080e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b080e-113">Requirement</span></span> | <span data-ttu-id="b080e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b080e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b080e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b080e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b080e-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b080e-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b080e-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b080e-117">Library</span></span><br/> | <dl> <span data-ttu-id="b080e-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b080e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b080e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b080e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b080e-120">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="b080e-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




