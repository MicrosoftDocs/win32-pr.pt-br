---
title: Como funciona o SNMP
description: Como um aplicativo de console de gerenciamento SNMP de terceiros retorna informações do serviço SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916131"
---
# <a name="how-snmp-works"></a><span data-ttu-id="6414e-103">Como funciona o SNMP</span><span class="sxs-lookup"><span data-stu-id="6414e-103">How SNMP Works</span></span>

<span data-ttu-id="6414e-104">As etapas a seguir descrevem como um aplicativo de console de gerenciamento SNMP de terceiros retorna informações do serviço SNMP:</span><span class="sxs-lookup"><span data-stu-id="6414e-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="6414e-105">O aplicativo de console de gerenciamento SNMP formula uma mensagem SNMP com base na entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="6414e-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="6414e-106">A mensagem inclui uma PDU (unidade de dados de protocolo) e informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6414e-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="6414e-107">O aplicativo de console de gerenciamento pode usar a biblioteca de API de gerenciamento SNMP da Microsoft (MGMTAPI.DLL) ou a biblioteca de API do Microsoft [WinSNMP](winsnmp-api.md) (WSNMP32.DLL) para executar essa etapa.</span><span class="sxs-lookup"><span data-stu-id="6414e-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="6414e-108">O aplicativo de console de gerenciamento SNMP envia a mensagem SNMP para o serviço SNMP, usando as bibliotecas de serviço SNMP.</span><span class="sxs-lookup"><span data-stu-id="6414e-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="6414e-109">O serviço SNMP recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6414e-109">The SNMP service receives the request.</span></span> <span data-ttu-id="6414e-110">Ele verifica as informações de autenticação e o endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="6414e-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="6414e-111">O serviço SNMP seleciona o agente de extensão apropriado e solicita que o agente recupere as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="6414e-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="6414e-112">O serviço SNMP envia a resposta para o aplicativo de console de gerenciamento SNMP.</span><span class="sxs-lookup"><span data-stu-id="6414e-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 




