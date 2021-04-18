---
description: Operações de bloqueio de Pseudoblocking no Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-bloqueio e verdadeiro bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807202"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="e00ef-103">Pseudo-bloqueio e verdadeiro bloqueio</span><span class="sxs-lookup"><span data-stu-id="e00ef-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="e00ef-104">Em 16 ambientes do Windows, o sistema operacional não dá suporte ao bloqueio verdadeiro. Portanto, uma operação de bloqueio que não pode ser concluída imediatamente é manipulada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e00ef-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="e00ef-105">O provedor de serviços inicia a operação e, em seguida, insere um loop durante o qual ele despacha qualquer mensagem do Windows (produzindo o processador para outro thread, se necessário)</span><span class="sxs-lookup"><span data-stu-id="e00ef-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="e00ef-106">Em seguida, ele verifica a conclusão da função do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="e00ef-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="e00ef-107">Se a função tiver sido concluída, ou se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) tiver sido invocado, o loop será encerrado e a função de bloqueio é concluída com um resultado apropriado.</span><span class="sxs-lookup"><span data-stu-id="e00ef-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="e00ef-108">Isso é o que se destina ao pseudodispositivo do termo, e o loop mencionado acima é conhecido como o gancho de bloqueio padrão.</span><span class="sxs-lookup"><span data-stu-id="e00ef-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
