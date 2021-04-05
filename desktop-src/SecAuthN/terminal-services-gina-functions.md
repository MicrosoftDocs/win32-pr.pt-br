---
description: Quando os serviços de terminal são habilitados, a GINA deve chamar funções de suporte do Winlogon para concluir a configuração de cada usuário, consultar as credenciais de uma sessão de cliente dos serviços de terminal e desconectar-se de uma sessão de rede dos serviços de terminal. Observe que as DLLs GINAs são ignoradas no Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Funções de GINA de serviços de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827029"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="09c16-103">Funções de GINA de serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="09c16-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="09c16-104">Quando os serviços de terminal são habilitados, a [*Gina*](../secgloss/g-gly.md) deve chamar funções de suporte do [*Winlogon*](../secgloss/w-gly.md) para concluir a configuração de cada usuário, consultar as [*credenciais*](../secgloss/c-gly.md) de uma sessão de cliente dos serviços de terminal e desconectar-se de uma sessão de rede dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="09c16-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="09c16-105">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09c16-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="09c16-106">Essas funções de suporte incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="09c16-106">These support functions include the following.</span></span>



| <span data-ttu-id="09c16-107">Função</span><span class="sxs-lookup"><span data-stu-id="09c16-107">Function</span></span>                                                                     | <span data-ttu-id="09c16-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="09c16-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09c16-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="09c16-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="09c16-110">Conclui a configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="09c16-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="09c16-111">**WlxQueryClientCredentials**</span><span class="sxs-lookup"><span data-stu-id="09c16-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="09c16-112">Chamado para consultar as credenciais de clientes remotos que não estão usando uma licença de conector da Internet.</span><span class="sxs-lookup"><span data-stu-id="09c16-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="09c16-113">**WlxQueryInetConnectorCredentials**</span><span class="sxs-lookup"><span data-stu-id="09c16-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="09c16-114">Chamado para consultar as credenciais de clientes remotos que estão usando uma licença de conector da Internet.</span><span class="sxs-lookup"><span data-stu-id="09c16-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="09c16-115">**WlxQueryTerminalServicesData**</span><span class="sxs-lookup"><span data-stu-id="09c16-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="09c16-116">Chamado para recuperar informações de configuração do usuário dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="09c16-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="09c16-117">**WlxDisconnect**</span><span class="sxs-lookup"><span data-stu-id="09c16-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="09c16-118">Chamado para desconectar-se de uma sessão de rede dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="09c16-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="09c16-119">Para acessar essas funções de suporte do Winlogon, a DLL GINA deve usar a estrutura de [**expedição WLX da \_ \_ versão \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) .</span><span class="sxs-lookup"><span data-stu-id="09c16-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="09c16-120">Na função [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) da Gina, ambos os parâmetros devem ser pelo menos WLX \_ versão \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="09c16-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
