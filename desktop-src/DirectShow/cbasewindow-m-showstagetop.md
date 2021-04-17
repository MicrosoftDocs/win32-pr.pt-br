---
description: Mensagem privada que define o estilo da janela como WS \_ ex mais \_ alta.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membro CBaseWindow:: m_ShowStageTop (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749624"
---
# <a name="cbasewindowm_showstagetop-member"></a><span data-ttu-id="a2449-103">Membro de CBaseWindow:: m \_ ShowStageTop</span><span class="sxs-lookup"><span data-stu-id="a2449-103">CBaseWindow::m\_ShowStageTop member</span></span>

<span data-ttu-id="a2449-104">Mensagem privada que define o estilo da janela como WS \_ ex mais \_ alta.</span><span class="sxs-lookup"><span data-stu-id="a2449-104">Private message that sets the window style to WS\_EX\_TOPMOST.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2449-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2449-105">Syntax</span></span>


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a><span data-ttu-id="a2449-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2449-106">Remarks</span></span>

<span data-ttu-id="a2449-107">Os renderizadores de vídeo devem enviar essa mensagem para a janela se mudarem para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="a2449-107">Video renderers should send this message to the window if they switch to full-screen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2449-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2449-108">Requirements</span></span>



| <span data-ttu-id="a2449-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2449-109">Requirement</span></span> | <span data-ttu-id="a2449-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a2449-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2449-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2449-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a2449-112"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2449-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2449-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2449-113">Library</span></span><br/> | <dl> <span data-ttu-id="a2449-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a2449-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2449-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2449-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2449-116">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a2449-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




