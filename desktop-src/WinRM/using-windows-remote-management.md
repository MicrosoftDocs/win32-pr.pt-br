---
title: Usando Gerenciamento Remoto do Windows
description: O Gerenciamento Remoto do Windows destina-se a melhorar o gerenciamento de hardware em um ambiente de rede com vários dispositivos que executam uma variedade de sistemas operacionais.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084723"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="8f180-103">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="8f180-103">Using Windows Remote Management</span></span>

<span data-ttu-id="8f180-104">O Gerenciamento Remoto do Windows destina-se a melhorar o gerenciamento de hardware em um ambiente de rede com vários dispositivos que executam uma variedade de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="8f180-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="8f180-105">Todo o projeto do serviço se concentra no monitoramento e gerenciamento de computadores remotos, implementando um protocolo padrão interoperável.</span><span class="sxs-lookup"><span data-stu-id="8f180-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="8f180-106">Como a [API de script do WinRM](winrm-scripting-api.md) e a [API do WinRM C++](winrm-c---api.md) implementam e modelam de forma minuciosa as operações definidas para o protocolo WS-Management, os scripts e os aplicativos recebem fluxos de XML em resposta a solicitações.</span><span class="sxs-lookup"><span data-stu-id="8f180-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="8f180-107">Os parâmetros de entrada para chamadas de método devem ser construídos em XML.</span><span class="sxs-lookup"><span data-stu-id="8f180-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="8f180-108">Você pode usar os métodos da API do [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para exibir ou construir cadeias de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="8f180-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="8f180-109">Para obter um exemplo, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="8f180-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="8f180-110">A lista a seguir inclui tópicos que descrevem como usar o script do WinRM:</span><span class="sxs-lookup"><span data-stu-id="8f180-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="8f180-111">Detectando se um computador remoto dá suporte ao protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="8f180-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="8f180-112">Obtendo dados do computador local</span><span class="sxs-lookup"><span data-stu-id="8f180-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="8f180-113">Obtendo dados de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="8f180-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="8f180-114">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="8f180-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="8f180-115">Consultando instâncias específicas de um recurso</span><span class="sxs-lookup"><span data-stu-id="8f180-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="8f180-116">Exibindo a saída XML de scripts do WinRM</span><span class="sxs-lookup"><span data-stu-id="8f180-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="8f180-117">Rastreando atividade do WinRM</span><span class="sxs-lookup"><span data-stu-id="8f180-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="8f180-118">Como o WinRM obtém dados por meio de [Instrumentação de gerenciamento do Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), você pode rastrear a atividade do WMI resultante de mensagens do WinRM.</span><span class="sxs-lookup"><span data-stu-id="8f180-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="8f180-119">A partir do Windows Vista, o serviço WMI não usa mais os [arquivos de log do WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="8f180-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="8f180-120">Em vez disso, ele usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e eventos estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando Evtutil.</span><span class="sxs-lookup"><span data-stu-id="8f180-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f180-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f180-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f180-122">Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="8f180-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="8f180-123">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="8f180-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="8f180-124">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="8f180-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="8f180-125">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="8f180-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 