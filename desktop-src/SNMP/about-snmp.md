---
title: Sobre SNMP
description: O SNMP usa uma arquitetura distribuída que consiste em gerentes e agentes.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007992"
---
# <a name="about-snmp"></a><span data-ttu-id="afb47-104">Sobre SNMP</span><span class="sxs-lookup"><span data-stu-id="afb47-104">About SNMP</span></span>

<span data-ttu-id="afb47-105">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="afb47-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="afb47-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="afb47-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="afb47-107">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="afb47-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="afb47-108">O SNMP usa uma arquitetura distribuída que consiste em gerentes e agentes.</span><span class="sxs-lookup"><span data-stu-id="afb47-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="afb47-109">Um agente é um aplicativo SNMP que responde a consultas de aplicativos do Gerenciador SNMP.</span><span class="sxs-lookup"><span data-stu-id="afb47-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="afb47-110">O agente SNMP é responsável por recuperar e atualizar informações de gerenciamento local com base nas solicitações do Gerenciador SNMP.</span><span class="sxs-lookup"><span data-stu-id="afb47-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="afb47-111">O agente também notifica os gerentes registrados quando ocorrem eventos ou interceptações significativos.</span><span class="sxs-lookup"><span data-stu-id="afb47-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="afb47-112">Um gerente é um aplicativo SNMP que gera consultas para aplicativos de agente SNMP e recebe interceptações de aplicativos de agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="afb47-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="afb47-113">Em computadores que executam o Microsoft Windows XP/Windows 2000/Windows NT, o agente SNMP é implementado pelo serviço SNMP (SNMP.EXE).</span><span class="sxs-lookup"><span data-stu-id="afb47-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="afb47-114">O Gerenciador SNMP normalmente é um aplicativo de console de gerenciamento SNMP de terceiros.</span><span class="sxs-lookup"><span data-stu-id="afb47-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="afb47-115">O aplicativo de console de gerenciamento não precisa ser executado no mesmo host que o agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="afb47-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="afb47-116">Para usar as informações fornecidas pelo serviço SNMP da Microsoft, você precisa de pelo menos um aplicativo de console de gerenciamento SNMP.</span><span class="sxs-lookup"><span data-stu-id="afb47-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="afb47-117">O sistema inclui bibliotecas que dão suporte a aplicativos de console de gerenciamento SNMP, mas não inclui um aplicativo de console de gerenciamento SNMP no momento.</span><span class="sxs-lookup"><span data-stu-id="afb47-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 