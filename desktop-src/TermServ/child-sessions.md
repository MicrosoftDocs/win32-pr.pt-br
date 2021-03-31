---
title: Sessões filho
description: A partir do Windows Server 2012 e do Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma sessão filho, que é uma sessão de Área de Trabalho Remota de loopback especial que está vinculada à sessão existente de um usuário.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159349"
---
# <a name="child-sessions"></a><span data-ttu-id="5e145-103">Sessões filho</span><span class="sxs-lookup"><span data-stu-id="5e145-103">Child Sessions</span></span>

<span data-ttu-id="5e145-104">A partir do Windows Server 2012 e do Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma *sessão filho*, que é uma sessão de área de trabalho remota de loopback especial que está vinculada à sessão existente de um usuário.</span><span class="sxs-lookup"><span data-stu-id="5e145-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="5e145-105">Não há suporte para sessões filhas nos seguintes sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="5e145-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="5e145-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="5e145-106">Windows RT</span></span>  
<span data-ttu-id="5e145-107">Opção de instalação do Windows Server 2012 Server Core</span><span class="sxs-lookup"><span data-stu-id="5e145-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="5e145-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e145-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="5e145-109">Um sistema pode ter apenas uma sessão filho ativa e conectada em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="5e145-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="5e145-110">A sessão filho pode ser finalizada fazendo logoff diretamente ou será encerrada quando a sessão pai for encerrada.</span><span class="sxs-lookup"><span data-stu-id="5e145-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="5e145-111">Antes que as sessões filho possam ser usadas em um sistema, você deve habilitar a funcionalidade de sessão filho chamando a função [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) .</span><span class="sxs-lookup"><span data-stu-id="5e145-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="5e145-112">Você também pode determinar se as sessões filhas foram habilitadas usando a função [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .</span><span class="sxs-lookup"><span data-stu-id="5e145-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="5e145-113">Uma sessão filho só pode ser criada de dentro de uma sessão de usuário existente usando o [controle ActiveX área de trabalho remota](remote-desktop-activex-control.md) e definindo a propriedade "ConnectToChildSession" com [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) antes da conexão.</span><span class="sxs-lookup"><span data-stu-id="5e145-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="5e145-114">Quando o método [**IMsTscAx. Connect**](imstscax-connect.md) for chamado, o controle ActiveX de área de trabalho remota fará logon automaticamente na sessão filho sem solicitar credenciais, exceto quando o usuário estiver conectado à sessão pai usando um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="5e145-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="5e145-115">Ao contrário de uma sessão de Área de Trabalho Remota regular, um usuário não precisa do direito interativo remoto de fazer logon na sessão filho porque esta é uma sessão de loopback.</span><span class="sxs-lookup"><span data-stu-id="5e145-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="5e145-116">Uma sessão filho não pode ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5e145-116">A child session cannot be locked.</span></span> <span data-ttu-id="5e145-117">Ele não terá proteção de tela nem nenhuma tela de logon.</span><span class="sxs-lookup"><span data-stu-id="5e145-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="5e145-118">Além disso, ao contrário de uma sessão regular, se a política de texto de logon do WinLogon for definida, o texto de logon não será exibido nessa sessão filho.</span><span class="sxs-lookup"><span data-stu-id="5e145-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="5e145-119">Além disso, não haverá nenhum efeito de Conexão de Área de Trabalho Remota políticas de grupo de tempo limite na sessão filho se essas políticas estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="5e145-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="5e145-120">As seguintes APIs são usadas em conjunto com sessões filho:</span><span class="sxs-lookup"><span data-stu-id="5e145-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="5e145-121">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="5e145-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="5e145-122">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5e145-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="5e145-123">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="5e145-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="5e145-124">Propriedade "ConnectToChildSession" em [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="5e145-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




