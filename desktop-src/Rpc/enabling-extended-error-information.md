---
title: Habilitando informações de erro estendidas
description: Habilitando informações de erro estendidas para RPC (chamada de procedimento remoto).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160071"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="a759c-103">Habilitando informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="a759c-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="a759c-104">Para habilitar as informações de erro estendidas, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a759c-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="a759c-105">Abra a política do computador local usando a interface gpedit. msc.</span><span class="sxs-lookup"><span data-stu-id="a759c-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="a759c-106">Navegue até a política localizada em configuração do computador/Modelos Administrativos/sistema/chamada de procedimento remoto/suporte para solução de problemas de RPC/propagação de informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="a759c-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="a759c-107">Habilite a política e defina a **propagação de campo de informações de erro estendidas** como "ativadas".</span><span class="sxs-lookup"><span data-stu-id="a759c-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="a759c-108">Esse processo ativa a propagação de informações de erro estendidas para todos os processos no computador.</span><span class="sxs-lookup"><span data-stu-id="a759c-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="a759c-109">Para habilitar informações de erro estendidas para apenas determinados processos em um computador ou para desabilitá-lo somente para determinados processos no computador, use as opções **desativar com exceções** ou **com exceções** .</span><span class="sxs-lookup"><span data-stu-id="a759c-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="a759c-110">As duas opções usam as **exceções de informações de erro estendidas** do campo para especificar quais processos têm a configuração padrão e quais processos têm o oposto da configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="a759c-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="a759c-111">**Exceções de informações de erro estendidas** contém uma lista de nomes de processo.</span><span class="sxs-lookup"><span data-stu-id="a759c-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="a759c-112">Se a linha de comando de um processo começar com uma cadeia de caracteres que está nas **exceções de informações de erro estendidas**, o processo receberá o oposto da configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="a759c-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="a759c-113">Por exemplo, se você quiser que todo o processo em seu computador propague informações de erro estendidas, exceto para LSASS e o processo chamado **servidor seguro**, defina a **propagação de informações de erro estendidas** como **ativado com exceções** e especifique no campo **exceções de informações de erro estendidas** a seguinte cadeia de caracteres: lsass "servidor seguro".</span><span class="sxs-lookup"><span data-stu-id="a759c-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="a759c-114">As cadeias de caracteres podem ser colocadas entre aspas duplas, mas isso é opcional se não houver nenhum espaço na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a759c-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="a759c-115">Além disso, o início da linha de comando do processo pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a759c-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="a759c-116">Por exemplo, se a **opção desativado com exceções** for especificada no campo **propagação de informações de erro estendidas** e no campo **exceções de informações de erro estendidas** , o seguinte será especificado: Win.</span><span class="sxs-lookup"><span data-stu-id="a759c-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="a759c-117">Cada processo que começa com "win" propaga informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="a759c-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="a759c-118">Em muitos computadores, por exemplo, esses processos seriam winlogon.exe e WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="a759c-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




