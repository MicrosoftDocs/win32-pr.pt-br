---
description: O status de energia do sistema indica se a fonte de energia de um computador é uma bateria do sistema ou uma energia CA. Para computadores que usam baterias, o status de energia do sistema também indica o quanto a vida útil da bateria permanece e se a bateria está carregando.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Status de energia do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778531"
---
# <a name="system-power-status"></a><span data-ttu-id="b8a0f-104">Status de energia do sistema</span><span class="sxs-lookup"><span data-stu-id="b8a0f-104">System Power Status</span></span>

<span data-ttu-id="b8a0f-105">O status de energia do sistema indica se a fonte de energia de um computador é uma bateria do sistema ou uma energia CA.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="b8a0f-106">Para computadores que usam baterias, o status de energia do sistema também indica o quanto a vida útil da bateria permanece e se a bateria está carregando.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="b8a0f-107">As informações de energia são recuperadas pelo registro para notificações de configuração de energia por meio da função [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) .</span><span class="sxs-lookup"><span data-stu-id="b8a0f-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="b8a0f-108">Essa função permite que os aplicativos se registrem em configurações de energia específicas e sejam notificados quando forem alterados.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="b8a0f-109">Para consultar informações de status de energia sem notificações, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span><span class="sxs-lookup"><span data-stu-id="b8a0f-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="b8a0f-110">Aplicativos e drivers instaláveis normalmente usam o status de energia do sistema para determinar se a operação contínua é viável.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="b8a0f-111">Por exemplo, antes que um aplicativo execute operações em segundo plano, como compactar ou paginar um arquivo, ele deve verificar se o sistema está em baterias.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="b8a0f-112">Como outro exemplo, um aplicativo que inicia uma operação demorada deve verificar o status para determinar se há energia suficiente de bateria para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="b8a0f-113">Por padrão, o sistema não consulta aplicativos ou drivers durante transições de suspensão.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="b8a0f-114">Se a energia for baixa, um aplicativo poderá solicitar a intervenção do usuário ou solicitar que o sistema se suspenda.</span><span class="sxs-lookup"><span data-stu-id="b8a0f-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="b8a0f-115">Você pode suspender a operação do sistema usando a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="b8a0f-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b8a0f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8a0f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8a0f-117">Sobre o gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="b8a0f-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



