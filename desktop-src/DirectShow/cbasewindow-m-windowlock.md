---
description: Seção crítica para serializar o acesso ao objeto.
ms.assetid: 24a5b1b2-209e-4262-aa48-fd4534b2da57
title: 'Membro CBaseWindow:: m_WindowLock (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WindowLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38227e505f2e05e024c8cecf12ab3cb8c336bfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759571"
---
# <a name="cbasewindowm_windowlock-member"></a><span data-ttu-id="66b00-103">Membro de CBaseWindow:: m \_ WindowLock</span><span class="sxs-lookup"><span data-stu-id="66b00-103">CBaseWindow::m\_WindowLock member</span></span>

<span data-ttu-id="66b00-104">Seção crítica para serializar o acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="66b00-104">Critical section, to serialize access to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66b00-105">Syntax</span></span>


```C++
CCritSec m_WindowLock;
```



## <a name="requirements"></a><span data-ttu-id="66b00-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b00-106">Requirements</span></span>



| <span data-ttu-id="66b00-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b00-107">Requirement</span></span> | <span data-ttu-id="66b00-108">Valor</span><span class="sxs-lookup"><span data-stu-id="66b00-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b00-109">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66b00-109">Header</span></span><br/>  | <dl> <span data-ttu-id="66b00-110"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66b00-110"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66b00-111">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66b00-111">Library</span></span><br/> | <dl> <span data-ttu-id="66b00-112"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66b00-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b00-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="66b00-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b00-114">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="66b00-114">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




