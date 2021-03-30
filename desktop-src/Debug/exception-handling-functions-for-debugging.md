---
description: Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador, passando a exceção para ele. Isso é conhecido como notificação de primeira chance. Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funções de manipulação de exceção para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826088"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="dd2ee-105">Funções de manipulação de exceção para depuração</span><span class="sxs-lookup"><span data-stu-id="dd2ee-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="dd2ee-106">Quando ocorre uma exceção em um processo que está sendo depurado, o sistema notifica o depurador, passando a exceção para ele.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="dd2ee-107">Isso é conhecido como *notificação de primeira chance*.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="dd2ee-108">Em seguida, o sistema suspende todos os threads no processo que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="dd2ee-109">Se o depurador não tratar a exceção, o sistema tentará localizar um manipulador de exceção apropriado.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="dd2ee-110">Se o sistema não conseguir localizar um apropriado, o sistema notificará novamente o depurador de que ocorreu uma exceção.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="dd2ee-111">Isso é conhecido como *notificação de última chance*.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="dd2ee-112">Se o depurador não tratar a exceção após a notificação de última chance, o sistema encerrará o processo que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="dd2ee-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="dd2ee-113">Para obter mais informações, consulte [manipulação de exceção do depurador](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="dd2ee-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



