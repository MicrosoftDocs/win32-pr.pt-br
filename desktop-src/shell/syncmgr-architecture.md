---
description: O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, diálogos de erro e caixas de diálogo de progresso.
title: Arquitetura do Gerenciador de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663491"
---
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="7b906-103">Arquitetura do Gerenciador de sincronização</span><span class="sxs-lookup"><span data-stu-id="7b906-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="7b906-104">O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, diálogos de erro e caixas de diálogo de progresso.</span><span class="sxs-lookup"><span data-stu-id="7b906-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="7b906-105">Com os componentes da interface do usuário, o usuário final pode agendar aplicativos para sincronização e configurar a sincronização automática para ocorrer em conjunto com os eventos do sistema especificados.</span><span class="sxs-lookup"><span data-stu-id="7b906-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="7b906-106">Por exemplo, o SyncMgr pode ser invocado no logon do usuário ou no desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="7b906-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="7b906-107">O usuário também pode invocar uma sincronização manual.</span><span class="sxs-lookup"><span data-stu-id="7b906-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="7b906-108">O usuário seleciona um aplicativo e especifica os itens dentro do aplicativo a ser sincronizado e define um evento de gatilho.</span><span class="sxs-lookup"><span data-stu-id="7b906-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="7b906-109">Por exemplo, em um aplicativo de email, a caixa de entrada, caixa de saída ou alguma outra pasta contendo mensagens pode ser um item separado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b906-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="7b906-110">O SyncMgr também inclui uma interface de programação para que os aplicativos possam se registrar para usar recursos de sincronização, podem processar erros e receber informações de progresso e notificações durante o processo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7b906-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



