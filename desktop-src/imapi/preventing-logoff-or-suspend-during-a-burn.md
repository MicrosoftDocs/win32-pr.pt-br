---
title: Impedindo o logoff ou a suspensão durante uma gravação
description: Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação. Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454004"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a><span data-ttu-id="b17e9-104">Impedindo o logoff ou a suspensão durante uma gravação</span><span class="sxs-lookup"><span data-stu-id="b17e9-104">Preventing Logoff or Suspend During a Burn</span></span>

<span data-ttu-id="b17e9-105">Se as precauções adequadas não forem feitas em um aplicativo, é possível que um usuário faça logoff durante uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="b17e9-105">If proper precautions are not made within an application, it is possible for a user to log off during a burn operation.</span></span> <span data-ttu-id="b17e9-106">Isso leva à interrupção do processo de gravação, o que pode resultar em perda de dados e possivelmente renderizar o disco inutilizável.</span><span class="sxs-lookup"><span data-stu-id="b17e9-106">This leads to the interruption of the burn process, which can result in lost data and possibly render the disc unusable.</span></span>

<span data-ttu-id="b17e9-107">Para evitar esse problema, o aplicativo deve processar a mensagem do [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) , que é entregue antes do logoff.</span><span class="sxs-lookup"><span data-stu-id="b17e9-107">To avoid this problem, the application should process the [**WM\_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) message which is delivered prior to log off.</span></span> <span data-ttu-id="b17e9-108">Se o aplicativo receber essa mensagem durante a execução de uma operação de gravação, retorne **false** para cancelar o procedimento de logoff.</span><span class="sxs-lookup"><span data-stu-id="b17e9-108">If the application receives this message while performing a burn operation, return **FALSE** to cancel the logoff procedure.</span></span> <span data-ttu-id="b17e9-109">Se o aplicativo permitir que o usuário decida se deseja continuar o logoff, será fornecido um aviso indicando que o usuário perderá os dados.</span><span class="sxs-lookup"><span data-stu-id="b17e9-109">If the application allows the user to decide whether to continue logging off, a warning should be provided indicating that user will lose data.</span></span>

<span data-ttu-id="b17e9-110">As transições de energia durante o processo de gravação também podem criar possíveis problemas no sucesso de uma atividade de gravação.</span><span class="sxs-lookup"><span data-stu-id="b17e9-110">Power transitions during the burn process can also create potential problems in the success of a burn activity.</span></span> <span data-ttu-id="b17e9-111">Impedir essas complicações durante o processo de gravação exige que um aplicativo esteja ciente de quando as transições de energia estão prestes a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="b17e9-111">Preventing these complications during the burn process requires an application to be aware of when power transitions are about to take place.</span></span> <span data-ttu-id="b17e9-112">Isso é feito por meio da habilitação do aplicativo para processar a mensagem [**\_ POWERBROADCAST do WM**](/windows/desktop/Power/wm-powerbroadcast) .</span><span class="sxs-lookup"><span data-stu-id="b17e9-112">This is accomplished by by enabling the application to process the [**WM\_POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) message.</span></span> <span data-ttu-id="b17e9-113">Os aplicativos desenvolvidos para o Windows XP ou o Windows Server 2003 podem retornar a **\_ \_ negação de consulta de difusão** em resposta ao [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), impedindo a suspensão durante o processo de gravação.</span><span class="sxs-lookup"><span data-stu-id="b17e9-113">Applications developed for Windows XP or Windows Server 2003 can return **BROADCAST\_QUERY\_DENY** in response to [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), preventing Suspend during the burn process.</span></span>

<span data-ttu-id="b17e9-114">Devido a alterações no modelo de gerenciamento de energia para Windows Vista e Windows Server 2008, o evento [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) não é mais entregue aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b17e9-114">Due to changes in the Power Management Model for Windows Vista and Windows Server 2008, the [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) event is no longer delivered to applications.</span></span> <span data-ttu-id="b17e9-115">Em vez disso, o evento [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) é entregue, fornecendo dois segundos para um aplicativo se preparar para a transição.</span><span class="sxs-lookup"><span data-stu-id="b17e9-115">Instead the [**PBT\_APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) event is delivered, providing two seconds for an application to prepare for the transition.</span></span>

<span data-ttu-id="b17e9-116">Como resultado dessas alterações, é recomendável que os aplicativos chamem a função [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) para evitar um tempo limite ocioso do sistema que normalmente resulta na transição para suspender.</span><span class="sxs-lookup"><span data-stu-id="b17e9-116">As a result of these changes, it is recommended that applications call the [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) function to prevent a system idle time-out which ordinarily results in the transition to Suspend.</span></span> <span data-ttu-id="b17e9-117">É importante lembrar que a chamada dessa função com os sinalizadores apropriados definidos só impedirá o sistema ocioso, e não uma suspensão em andamento.</span><span class="sxs-lookup"><span data-stu-id="b17e9-117">It is important to remember that calling this function with the appropriate flags set will only prevent system idle, not an in-progress Suspend.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b17e9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b17e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b17e9-119">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="b17e9-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="b17e9-120">**SetThreadExecutionState**</span><span class="sxs-lookup"><span data-stu-id="b17e9-120">**SetThreadExecutionState**</span></span>](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 