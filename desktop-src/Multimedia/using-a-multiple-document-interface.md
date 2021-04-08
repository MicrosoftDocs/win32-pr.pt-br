---
title: Usando uma interface de vários documentos
description: Usando uma interface de vários documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Função MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823735"
---
# <a name="using-a-multiple-document-interface"></a><span data-ttu-id="9d552-104">Usando uma interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="9d552-104">Using a Multiple Document Interface</span></span>

<span data-ttu-id="9d552-105">Os aplicativos que usam uma MDI (interface de vários documentos) podem precisar especificar estilos de janela que não estão disponíveis por meio da função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="9d552-105">Applications that use a multiple document interface (MDI) might need to specify window styles that are not available through the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="9d552-106">Para esses aplicativos, você pode registrar e criar uma janela MCIWnd usando a função [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) com a função [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="9d552-106">For these applications, you can register and create an MCIWnd window by using the [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) function with the [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="9d552-107">A função **MCIWndRegisterClass** registra a classe da janela da \_ classe MCIWND Window \_ e, em seguida, **CreateWindowEx** cria uma instância de uma janela MCIWND.</span><span class="sxs-lookup"><span data-stu-id="9d552-107">The **MCIWndRegisterClass** function registers the MCIWND\_WINDOW\_CLASS window class and then **CreateWindowEx** creates an instance of an MCIWnd window.</span></span>

 

 