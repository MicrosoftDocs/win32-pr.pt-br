---
title: Macros
description: Os tópicos nesta seção fornecem as especificações de referência para mensagens de entrada de ponteiro e macros de notificações para recuperar informações de parâmetros de mensagem de entrada de ponteiro.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2020
ms.locfileid: "104365446"
---
# <a name="macros"></a><span data-ttu-id="f29b5-103">Macros</span><span class="sxs-lookup"><span data-stu-id="f29b5-103">Macros</span></span>

<span data-ttu-id="f29b5-104">Os tópicos nesta seção fornecem as especificações de referência para [mensagens de entrada de ponteiro e](messages-and-notifications-portal.md) macros de notificações para recuperar informações de parâmetros de mensagem de entrada de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f29b5-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f29b5-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f29b5-105">In this section</span></span>



| <span data-ttu-id="f29b5-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="f29b5-106">Topic</span></span>                                                                                  | <span data-ttu-id="f29b5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f29b5-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f29b5-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="f29b5-109">Recupera a ID do ponteiro usando o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f29b5-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="f29b5-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="f29b5-111">Verifica se a mensagem de ponteiro especificada é considerada intencional em vez de acidental.</span><span class="sxs-lookup"><span data-stu-id="f29b5-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="f29b5-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="f29b5-113">Verifica se a entrada do ponteiro especificada foi encerrada abruptamente ou se era inválida, indicando que a interação não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f29b5-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="f29b5-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="f29b5-115">Verifica se o ponteiro especificado executou a quinta ação.</span><span class="sxs-lookup"><span data-stu-id="f29b5-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="f29b5-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="f29b5-117">Verifica se o ponteiro especificado realizou a primeira ação.</span><span class="sxs-lookup"><span data-stu-id="f29b5-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="f29b5-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="f29b5-119">Verifica se uma macro de ponteiro define o sinalizador especificado.</span><span class="sxs-lookup"><span data-stu-id="f29b5-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="f29b5-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="f29b5-121">Verifica se o ponteiro especificado executou a quarta ação.</span><span class="sxs-lookup"><span data-stu-id="f29b5-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="f29b5-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="f29b5-123">Verifica se o ponteiro especificado está em contato.</span><span class="sxs-lookup"><span data-stu-id="f29b5-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="f29b5-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="f29b5-125">Verifica se o ponteiro especificado está no intervalo.</span><span class="sxs-lookup"><span data-stu-id="f29b5-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="f29b5-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="f29b5-127">Verifica se o ponteiro especificado é um novo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f29b5-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="f29b5-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="f29b5-129">Verifica se o ponteiro especificado é o ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="f29b5-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="f29b5-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="f29b5-131">Verifica se o ponteiro especificado executou a segunda ação.</span><span class="sxs-lookup"><span data-stu-id="f29b5-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="f29b5-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f29b5-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="f29b5-133">Verifica se o ponteiro especificado executou a terceira ação.</span><span class="sxs-lookup"><span data-stu-id="f29b5-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="f29b5-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f29b5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f29b5-135">Referência de mensagem de entrada do ponteiro</span><span class="sxs-lookup"><span data-stu-id="f29b5-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





