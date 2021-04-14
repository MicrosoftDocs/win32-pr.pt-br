---
title: O banco de dados WinSNMP
description: A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453559"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="8623a-103">O banco de dados WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8623a-103">The WinSNMP Database</span></span>

<span data-ttu-id="8623a-104">A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8623a-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="8623a-105">O banco de dados inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="8623a-105">The database includes the following information:</span></span>

-   <span data-ttu-id="8623a-106">Propriedades de rede e versão.</span><span class="sxs-lookup"><span data-stu-id="8623a-106">Network and version properties.</span></span>

    <span data-ttu-id="8623a-107">A implementação usa essas propriedades para determinar qual protocolo de transporte de rede e a estrutura de versão SNMP usar para concluir solicitações de transmissão.</span><span class="sxs-lookup"><span data-stu-id="8623a-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="8623a-108">Para obter mais informações, consulte [sobre as versões SNMP](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="8623a-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="8623a-109">Modo de tradução de contexto e entidade.</span><span class="sxs-lookup"><span data-stu-id="8623a-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="8623a-110">A implementação usa esse modo para interpretar nomes amigáveis para entidades e contextos SNMP.</span><span class="sxs-lookup"><span data-stu-id="8623a-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="8623a-111">Para obter mais informações, consulte [definindo a entidade e o modo de tradução de contexto](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="8623a-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="8623a-112">Configuração de política de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="8623a-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="8623a-113">A implementação usa essa configuração para determinar se ela deve ou não executar a política de retransmissão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8623a-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="8623a-114">A implementação armazena um valor de tempo limite e uma contagem de repetição para cada entidade de destino.</span><span class="sxs-lookup"><span data-stu-id="8623a-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="8623a-115">Para obter mais informações, consulte [sobre a retransmissão](about-retransmission.md) e [Gerenciamento da política de retransmissão](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8623a-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




