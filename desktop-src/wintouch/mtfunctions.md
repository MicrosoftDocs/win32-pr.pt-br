---
title: Funções (entrada do Windows Touch)
description: Esta seção contém funções para entrada do Windows Touch.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows Touch, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008778"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="64a1e-104">Funções (entrada do Windows Touch)</span><span class="sxs-lookup"><span data-stu-id="64a1e-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="64a1e-105">Esta seção contém funções para entrada do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="64a1e-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="64a1e-106">As funções a seguir são usadas para a entrada do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="64a1e-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="64a1e-107">Função</span><span class="sxs-lookup"><span data-stu-id="64a1e-107">Function</span></span>                                                                                               | <span data-ttu-id="64a1e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="64a1e-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64a1e-109">**CloseTouchInputHandle**</span><span class="sxs-lookup"><span data-stu-id="64a1e-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="64a1e-110">Fecha um identificador de entrada por toque, libera a memória de processo associada a ele e invalida o identificador.</span><span class="sxs-lookup"><span data-stu-id="64a1e-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="64a1e-111">**GetTouchInputInfo**</span><span class="sxs-lookup"><span data-stu-id="64a1e-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="64a1e-112">Recupera informações detalhadas sobre as entradas de toque associadas a um identificador de entrada de toque específico.</span><span class="sxs-lookup"><span data-stu-id="64a1e-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="64a1e-113">**IsTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="64a1e-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="64a1e-114">Verifica se uma janela especificada é compatível com toque e, opcionalmente, recupera os sinalizadores modificadores definidos para o recurso de toque da janela.</span><span class="sxs-lookup"><span data-stu-id="64a1e-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="64a1e-115">**RegisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="64a1e-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="64a1e-116">Registra uma janela como sendo compatível com toque.</span><span class="sxs-lookup"><span data-stu-id="64a1e-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="64a1e-117">**UnregisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="64a1e-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="64a1e-118">Registra uma janela como não está mais sendo compatível com toque.</span><span class="sxs-lookup"><span data-stu-id="64a1e-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="64a1e-119">SendMessage, mensagem de mensagens e funções relacionadas</span><span class="sxs-lookup"><span data-stu-id="64a1e-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="64a1e-120">Contém considerações sobre o encaminhamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="64a1e-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="64a1e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64a1e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a1e-122">Entrada por toque do Windows</span><span class="sxs-lookup"><span data-stu-id="64a1e-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="64a1e-123">Guia de programação de entrada do Windows Touch</span><span class="sxs-lookup"><span data-stu-id="64a1e-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 




