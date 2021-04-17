---
description: Sinalizador que especifica se a janela publica ou envia sua mensagem de destruição.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749841"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="7c483-103">Membro de CBaseWindow:: m \_ bDoPostToDestroy</span><span class="sxs-lookup"><span data-stu-id="7c483-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="7c483-104">Sinalizador que especifica se a janela publica ou envia sua mensagem de destruição.</span><span class="sxs-lookup"><span data-stu-id="7c483-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="7c483-105">Se **for true**, o método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usará a função **CreateMessage** para enviar a si mesmo uma mensagem de destruição privada.</span><span class="sxs-lookup"><span data-stu-id="7c483-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="7c483-106">Se **for false**, **DoneWithWindow** usará a função **SendMessage** para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="7c483-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="7c483-107">Por padrão, o valor é **false**.</span><span class="sxs-lookup"><span data-stu-id="7c483-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c483-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c483-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="7c483-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c483-109">Requirements</span></span>



| <span data-ttu-id="7c483-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c483-110">Requirement</span></span> | <span data-ttu-id="7c483-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7c483-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c483-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c483-112">Header</span></span><br/>  | <dl> <span data-ttu-id="7c483-113"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c483-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c483-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c483-114">Library</span></span><br/> | <dl> <span data-ttu-id="7c483-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7c483-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c483-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c483-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c483-117">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="7c483-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




