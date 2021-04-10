---
title: Conexão de thread com uma área de trabalho
description: Depois que um processo se conecta a uma estação de janela, o sistema atribui uma área de trabalho ao thread que faz a conexão.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162304"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="03309-103">Conexão de thread com uma área de trabalho</span><span class="sxs-lookup"><span data-stu-id="03309-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="03309-104">Depois que um processo se conecta a uma estação de janela, o sistema atribui uma área de trabalho ao thread que faz a conexão.</span><span class="sxs-lookup"><span data-stu-id="03309-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="03309-105">O sistema determina a área de trabalho a ser atribuída ao thread de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="03309-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="03309-106">Se o thread tiver chamado a função [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , ele se conectará à área de trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="03309-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="03309-107">Se o thread não chamou [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), ele se conecta ao desktop herdado do processo pai.</span><span class="sxs-lookup"><span data-stu-id="03309-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="03309-108">Se o thread não chamou [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) e não herdou uma área de trabalho, o sistema tenta abrir para o máximo de \_ acesso permitido e se conectar a uma área de trabalho da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03309-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="03309-109">Se um nome de área de trabalho tiver sido especificado no membro **lpDesktop** da estrutura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que foi usada quando o processo foi criado, o thread se conectará à área de trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="03309-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="03309-110">Caso contrário, o thread se conecta à área de trabalho padrão da estação de janela à qual o processo está conectado.</span><span class="sxs-lookup"><span data-stu-id="03309-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="03309-111">A área de trabalho atribuída durante esse processo de conexão não pode ser fechada chamando a função [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .</span><span class="sxs-lookup"><span data-stu-id="03309-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="03309-112">Quando um processo está se conectando a uma área de trabalho, o sistema pesquisa a tabela identificador do processo em busca de identificadores herdados.</span><span class="sxs-lookup"><span data-stu-id="03309-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="03309-113">O sistema usa o primeiro identificador de área de trabalho que encontra.</span><span class="sxs-lookup"><span data-stu-id="03309-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="03309-114">Se você quiser que um processo filho se conecte a uma área de trabalho herdada específica, certifique-se de que o único identificador desejado esteja marcado como herdável.</span><span class="sxs-lookup"><span data-stu-id="03309-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="03309-115">Se um processo filho herdar vários identificadores de área de trabalho, os resultados da conexão de área de trabalho serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="03309-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="03309-116">Os identificadores para um desktop que o sistema abre ao conectar um processo a uma área de trabalho não são herdáveis.</span><span class="sxs-lookup"><span data-stu-id="03309-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03309-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03309-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03309-118">Processar conexão com uma estação de janela</span><span class="sxs-lookup"><span data-stu-id="03309-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 