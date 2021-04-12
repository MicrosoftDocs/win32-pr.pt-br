---
title: Operações de rede do Windows
description: Um aplicativo pode usar as funções WNet para procurar, adicionar ou cancelar conexões de rede em qualquer lugar na hierarquia de rede.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294171"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="75a22-103">Operações de rede do Windows</span><span class="sxs-lookup"><span data-stu-id="75a22-103">Windows Networking Operations</span></span>

<span data-ttu-id="75a22-104">Um aplicativo pode usar as funções WNet para procurar, adicionar ou cancelar conexões de rede em qualquer lugar na hierarquia de rede.</span><span class="sxs-lookup"><span data-stu-id="75a22-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="75a22-105">Uma *conexão persistente* é uma conexão de rede que o sistema restaura automaticamente quando o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="75a22-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="75a22-106">Você pode chamar as funções [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) para controlar se uma conexão de rede é persistente de uma sessão para a próxima.</span><span class="sxs-lookup"><span data-stu-id="75a22-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="75a22-107">Para localizar o nome de usuário padrão ou o nome de usuário usado para estabelecer uma conexão de rede, chame a função [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="75a22-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="75a22-108">Além de chamar as funções WNet, um processo também pode usar processadores e pipes nomeados para se comunicar com outro processo.</span><span class="sxs-lookup"><span data-stu-id="75a22-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="75a22-109">Para obter mais informações, consulte [processadores](/windows/desktop/ipc/mailslots) e [pipes](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="75a22-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 