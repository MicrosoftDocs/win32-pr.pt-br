---
description: A rotina de retorno de chamada de fila padrão manipula as notificações enviadas pelo SetupCommitFileQueue de maneira genérica.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Sobre a rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827019"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="6930d-103">Sobre a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="6930d-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="6930d-104">A rotina de retorno de chamada de fila padrão manipula as notificações enviadas pelo [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de maneira genérica.</span><span class="sxs-lookup"><span data-stu-id="6930d-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="6930d-105">Usando a rotina padrão, você obtém uma interface do usuário pronta para criar caixas de diálogo de instalação comuns.</span><span class="sxs-lookup"><span data-stu-id="6930d-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="6930d-106">É recomendável que você use a rotina de retorno de chamada de fila padrão, tanto para facilitar o uso quanto para garantir uma aparência e comportamento consistentes das caixas de diálogo geradas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6930d-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="6930d-107">A rotina de retorno de chamada padrão requer uma estrutura de contexto para manter o registro interno.</span><span class="sxs-lookup"><span data-stu-id="6930d-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="6930d-108">Além disso, a fila passa informações adicionais relevantes para a notificação atual em um conjunto de parâmetros, *param1* e *param2*.</span><span class="sxs-lookup"><span data-stu-id="6930d-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="6930d-109">Por exemplo, se a fila enviar uma \_ notificação SPFILENOTIFY NEEDMEDIA para a rotina de retorno de chamada padrão, o *param1* apontará para uma estrutura de [**\_ mídia de origem**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) que contém informações sobre a mídia necessária e *param2* aponta para uma matriz de caracteres que pode receber novas informações de caminho do usuário.</span><span class="sxs-lookup"><span data-stu-id="6930d-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="6930d-110">A rotina de retorno de chamada padrão usa essas informações para solicitar que o usuário insira a mídia de origem necessária, especifique um novo caminho, ignore a cópia do arquivo atual ou cancele a operação atual.</span><span class="sxs-lookup"><span data-stu-id="6930d-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="6930d-111">A rotina de retorno de chamada de fila padrão retorna FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ Skip ou FILEOP \_ Abort para a fila, dependendo de qual ação o usuário realizou.</span><span class="sxs-lookup"><span data-stu-id="6930d-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="6930d-112">Para obter informações sobre como a rotina de retorno de chamada de fila padrão manipula cada notificação de fila, consulte [notificações de fila de arquivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6930d-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="6930d-113">Para obter informações sobre rotinas de retorno de chamada de fila personalizada, consulte [criando uma rotina de retorno de chamada de fila personalizada](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="6930d-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



