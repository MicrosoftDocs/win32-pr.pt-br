---
description: O método DoSetWindowForeground traz a janela para o primeiro plano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Método CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751696"
---
# <a name="cbasewindowdosetwindowforeground-method"></a><span data-ttu-id="491fe-103">Método CBaseWindow. DoSetWindowForeground</span><span class="sxs-lookup"><span data-stu-id="491fe-103">CBaseWindow.DoSetWindowForeground method</span></span>

<span data-ttu-id="491fe-104">O `DoSetWindowForeground` método leva a janela para o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="491fe-104">The `DoSetWindowForeground` method brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="491fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="491fe-105">Syntax</span></span>


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a><span data-ttu-id="491fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="491fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="491fe-107">*bFocus*</span><span class="sxs-lookup"><span data-stu-id="491fe-107">*bFocus*</span></span> 
</dt> <dd>

<span data-ttu-id="491fe-108">Valor booliano que especifica se o foco da janela deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="491fe-108">Boolean value that specifies whether to give the window focus.</span></span> <span data-ttu-id="491fe-109">Se o valor for **true**, a janela ganha foco.</span><span class="sxs-lookup"><span data-stu-id="491fe-109">If the value is **TRUE**, the window gains focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="491fe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="491fe-110">Return value</span></span>

<span data-ttu-id="491fe-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="491fe-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="491fe-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="491fe-112">Requirements</span></span>



| <span data-ttu-id="491fe-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="491fe-113">Requirement</span></span> | <span data-ttu-id="491fe-114">Valor</span><span class="sxs-lookup"><span data-stu-id="491fe-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="491fe-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="491fe-115">Header</span></span><br/>  | <dl> <span data-ttu-id="491fe-116"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="491fe-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="491fe-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="491fe-117">Library</span></span><br/> | <dl> <span data-ttu-id="491fe-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="491fe-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491fe-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="491fe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491fe-120">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="491fe-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




