---
description: As atualizações que exigem a interação do usuário não poderão ser instaladas por aplicativos do Windows Update Agent (WUA) se os aplicativos do WUA estiverem em execução no contexto do serviço de logon secundário.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usando o WUA de um processo de logon secundário (executar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807197"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="36850-103">Usando o WUA de um processo de logon secundário (executar como)</span><span class="sxs-lookup"><span data-stu-id="36850-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="36850-104">As atualizações que exigem a interação do usuário não poderão ser instaladas por aplicativos do Windows Update Agent (WUA) se os aplicativos do WUA estiverem em execução no contexto do serviço de logon secundário.</span><span class="sxs-lookup"><span data-stu-id="36850-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="36850-105">Se o processo que está chamando o WUA estiver em execução no contexto do serviço RunAs ou do serviço de logon secundário, uma tentativa de instalar uma atualização que exige a interação do usuário falhará e retornará o erro de **\_ \_ \_ \_ usuário interativo e nenhum** .</span><span class="sxs-lookup"><span data-stu-id="36850-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="36850-106">No Microsoft Windows, você pode executar programas como um usuário que difere do usuário que está conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="36850-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="36850-107">Para fazer isso, o serviço de logon secundário deve estar em execução.</span><span class="sxs-lookup"><span data-stu-id="36850-107">To do this the Secondary Logon service must be running.</span></span>

 

 



