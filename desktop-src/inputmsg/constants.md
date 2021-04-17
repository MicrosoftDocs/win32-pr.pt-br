---
title: Constantes de mensagens e notificações de entrada de ponteiro
description: Os tópicos nesta seção fornecem as especificações de referência para as mensagens de entrada do ponteiro e as constantes de notificações.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188031"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="29e03-103">Constantes de mensagens e notificações de entrada de ponteiro</span><span class="sxs-lookup"><span data-stu-id="29e03-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="29e03-104">Os tópicos nesta seção fornecem as especificações de referência para [as mensagens de entrada do ponteiro e as](messages-and-notifications-portal.md) constantes de notificações.</span><span class="sxs-lookup"><span data-stu-id="29e03-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29e03-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="29e03-105">In this section</span></span>



| <span data-ttu-id="29e03-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="29e03-106">Topic</span></span>                                                                             | <span data-ttu-id="29e03-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="29e03-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29e03-108">**Estado de chave do modificador**</span><span class="sxs-lookup"><span data-stu-id="29e03-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="29e03-109">Indica quais teclas modificadoras de teclado foram pressionadas na hora em que a entrada estava sendo gerada.</span><span class="sxs-lookup"><span data-stu-id="29e03-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="29e03-110">**Sinalizadores de caneta**</span><span class="sxs-lookup"><span data-stu-id="29e03-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="29e03-111">Os valores que podem aparecer no campo **penFlags** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="29e03-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="29e03-112">**Máscara de caneta**</span><span class="sxs-lookup"><span data-stu-id="29e03-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="29e03-113">Os valores que podem aparecer no campo **penMask** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="29e03-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="29e03-114">**Alteração do dispositivo do ponteiro**</span><span class="sxs-lookup"><span data-stu-id="29e03-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="29e03-115">Valores que podem ser passados no parâmetro *wParam* da mensagem de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="29e03-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="29e03-116">**Sinalizadores de ponteiro**</span><span class="sxs-lookup"><span data-stu-id="29e03-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="29e03-117">Os valores que podem aparecer no campo **pointerFlags** da estrutura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="29e03-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="29e03-118">**Sinalizadores de mensagem do ponteiro**</span><span class="sxs-lookup"><span data-stu-id="29e03-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="29e03-119">Valores que são usados em várias macros de ponteiro (consulte [as macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="29e03-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="29e03-120">**Sinalizadores de toque**</span><span class="sxs-lookup"><span data-stu-id="29e03-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="29e03-121">Os valores que podem aparecer no campo **touchFlags** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="29e03-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="29e03-122">**Janela teste de colisão de toque**</span><span class="sxs-lookup"><span data-stu-id="29e03-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="29e03-123">Indica como as mensagens para teste de clique de toque são processadas pelo Windows que são registradas por meio da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="29e03-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="29e03-124">**Máscara de toque**</span><span class="sxs-lookup"><span data-stu-id="29e03-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="29e03-125">Os valores que podem aparecer no campo **touchMask** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="29e03-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="29e03-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29e03-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29e03-127">Referência de mensagem de entrada do ponteiro</span><span class="sxs-lookup"><span data-stu-id="29e03-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

