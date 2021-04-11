---
description: Para notificar o usuário de que ocorreu algum tipo de erro, muitos aplicativos simplesmente produzem um som usando a função MessageBeep ou piscam a janela usando a função FlashWindow ou FlashWindowEx.
ms.assetid: 35b6e93c-323a-4592-9394-a2e9dd79d9e6
title: Notificando o usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01a4e68b0c5dffcc5dcae5f2fe3b0c84288f59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163922"
---
# <a name="notifying-the-user"></a><span data-ttu-id="44d5a-103">Notificando o usuário</span><span class="sxs-lookup"><span data-stu-id="44d5a-103">Notifying the User</span></span>

<span data-ttu-id="44d5a-104">Para notificar o usuário de que ocorreu algum tipo de erro, muitos aplicativos simplesmente produzem um som usando a função [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) ou piscam a janela usando a função [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) ou [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) .</span><span class="sxs-lookup"><span data-stu-id="44d5a-104">To notify the user that some kind of error has occurred, many applications simply produce a sound by using the [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) function or flash the window by using either the [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) or [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) function.</span></span> <span data-ttu-id="44d5a-105">Um aplicativo também pode usar essas funções para chamar a atenção para um erro e, em seguida, exibir uma caixa de mensagem ou uma mensagem de erro contendo detalhes sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="44d5a-105">An application can also use these functions to call attention to an error and then display a message box or an error message containing details about the error.</span></span>

 

 



