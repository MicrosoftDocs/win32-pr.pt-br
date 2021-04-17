---
description: Mensagem privada que traz a janela para o primeiro plano.
ms.assetid: 88b28888-d729-4cf3-8b9d-618dbe150926
title: 'Membro CBaseWindow:: m_ShowStageMessage (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageMessage
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccf358eba577c0ee950f8628090a2f3024297fe3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789715"
---
# <a name="cbasewindowm_showstagemessage-member"></a><span data-ttu-id="20f6b-103">Membro de CBaseWindow:: m \_ ShowStageMessage</span><span class="sxs-lookup"><span data-stu-id="20f6b-103">CBaseWindow::m\_ShowStageMessage member</span></span>

<span data-ttu-id="20f6b-104">Mensagem privada que traz a janela para o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="20f6b-104">Private message that brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20f6b-105">Syntax</span></span>


```C++
UINT m_ShowStageMessage;
```



## <a name="remarks"></a><span data-ttu-id="20f6b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="20f6b-106">Remarks</span></span>

<span data-ttu-id="20f6b-107">O método [**CBaseWindow::D osetwindowforeground**](cbasewindow-dosetwindowforeground.md) envia essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="20f6b-107">The [**CBaseWindow::DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md) method sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f6b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f6b-108">Requirements</span></span>



| <span data-ttu-id="20f6b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f6b-109">Requirement</span></span> | <span data-ttu-id="20f6b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="20f6b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f6b-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f6b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="20f6b-112"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20f6b-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20f6b-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20f6b-113">Library</span></span><br/> | <dl> <span data-ttu-id="20f6b-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="20f6b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f6b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f6b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f6b-116">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="20f6b-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




