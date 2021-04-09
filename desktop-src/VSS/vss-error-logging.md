---
description: 'As seguintes informações de erro e estado do VSS são gravadas no log de eventos do aplicativo:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Log de erros do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090445"
---
# <a name="vss-error-logging"></a><span data-ttu-id="3a3c1-103">Log de erros do VSS</span><span class="sxs-lookup"><span data-stu-id="3a3c1-103">VSS Error Logging</span></span>

<span data-ttu-id="3a3c1-104">As seguintes informações de erro e estado do VSS são gravadas no log de eventos do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="3a3c1-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="3a3c1-105">Erros do solicitante produzidos usando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="3a3c1-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="3a3c1-106">Erros de gravador produzidos no usando a classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , incluindo métodos de substituição</span><span class="sxs-lookup"><span data-stu-id="3a3c1-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="3a3c1-107">Erros gerados pelo provedor padrão</span><span class="sxs-lookup"><span data-stu-id="3a3c1-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="3a3c1-108">Erros de serviço VSS gerados no provedor de coordenação, no gravador e na atividade do solicitante (como a geração de eventos)</span><span class="sxs-lookup"><span data-stu-id="3a3c1-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="3a3c1-109">Esses erros podem ter várias causas, incluindo um erro de programação em código de terceiros ou erros de configuração relacionados ao VSS.</span><span class="sxs-lookup"><span data-stu-id="3a3c1-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="3a3c1-110">Os drivers VSS e a funcionalidade de implementação de nível inferior gravam erros no log do sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3c1-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="3a3c1-111">Software de terceiros (solicitante, provedor, gravador) pode escolher o log do aplicativo, o log do sistema ou ambos, para gravar entradas do log de erros.</span><span class="sxs-lookup"><span data-stu-id="3a3c1-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="3a3c1-112">É recomendável que aplicativos de alto nível (como código de modo de usuário) usem o log do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a3c1-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="3a3c1-113">Aplicativos de nível inferior, como interfaces de hardware e drivers, devem usar o log do sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3c1-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



