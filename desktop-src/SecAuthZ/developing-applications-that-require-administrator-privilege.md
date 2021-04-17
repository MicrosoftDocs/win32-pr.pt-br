---
description: É possível desenvolver um aplicativo que executa operações que exigem privilégios de administrador, ainda que sejam executadas como um usuário padrão.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Desenvolvendo aplicativos que exigem privilégios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751609"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="a0821-103">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="a0821-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="a0821-104">É possível desenvolver um aplicativo que executa operações que exigem privilégios de administrador, ainda que sejam executadas como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="a0821-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="a0821-105">Há vários modelos para realizar isso.</span><span class="sxs-lookup"><span data-stu-id="a0821-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="a0821-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="a0821-106">Topic</span></span>                                                                | <span data-ttu-id="a0821-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0821-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0821-108">Modelo de tarefa elevada</span><span class="sxs-lookup"><span data-stu-id="a0821-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="a0821-109">Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="a0821-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="a0821-110">Modelo de serviço do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a0821-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="a0821-111">Um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como **sistema** usando RPC ( [chamada de procedimento remoto](/windows/desktop/Rpc/rpc-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="a0821-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="a0821-112">Modelo de agente do administrador</span><span class="sxs-lookup"><span data-stu-id="a0821-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="a0821-113">O aplicativo é dividido em dois programas.</span><span class="sxs-lookup"><span data-stu-id="a0821-113">The application is divided into two programs.</span></span> <span data-ttu-id="a0821-114">Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.</span><span class="sxs-lookup"><span data-stu-id="a0821-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="a0821-115">Modelo de objeto COM do administrador</span><span class="sxs-lookup"><span data-stu-id="a0821-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="a0821-116">Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador criando um objeto de [Component Object Model](/windows/desktop/com/component-object-model--com--portal) elevado.</span><span class="sxs-lookup"><span data-stu-id="a0821-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
