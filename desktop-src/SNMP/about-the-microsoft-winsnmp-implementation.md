---
title: Sobre a implementação do Microsoft WinSNMP
description: A implementação do Microsoft WinSNMP está em conformidade com o WinSNMP versão 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915865"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="717ee-103">Sobre a implementação do Microsoft WinSNMP</span><span class="sxs-lookup"><span data-stu-id="717ee-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="717ee-104">A implementação do Microsoft WinSNMP está em conformidade com o WinSNMP versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ee-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="717ee-105">Ele dá suporte a todas as funções e operações definidas na especificação do WinSNMP versão 1.1 a e no adendo do WinSNMP versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ee-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="717ee-106">A implementação fornece os seguintes serviços para aplicativos de WinSNMP:</span><span class="sxs-lookup"><span data-stu-id="717ee-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="717ee-107">Gerencia comunicações de e para entidades de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="717ee-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="717ee-108">A entidade pode residir no computador local ou estar conectada por meio de uma rede local ou de longa distância, ou a Internet.</span><span class="sxs-lookup"><span data-stu-id="717ee-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="717ee-109">Para obter mais informações, consulte [níveis de suporte a SNMP](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="717ee-110">Oculta os detalhes do protocolo SNMP, da notação de sintaxe abstrata um (ASN. 1) e as regras de codificação básica (BER) para descrever a sintaxe de transferência.</span><span class="sxs-lookup"><span data-stu-id="717ee-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="717ee-111">Verifica a exatidão de PDUs e rejeita PDUs inválidas.</span><span class="sxs-lookup"><span data-stu-id="717ee-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="717ee-112">Para obter mais informações, consulte [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="717ee-113">Transforma os tipos de PDU do SNMPv2C quando necessário de acordo com as RFCs relevantes.</span><span class="sxs-lookup"><span data-stu-id="717ee-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="717ee-114">Converte as armadilhas de SNMPv1 de um agente SNMPv1 em interceptações de SNMPv2C de acordo com a RFC 1908, "coexistência entre a versão 1 e a versão 2 da estrutura de gerenciamento de rede padrão da Internet".</span><span class="sxs-lookup"><span data-stu-id="717ee-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="717ee-115">Para obter mais informações, consulte [convertendo interceptações de SNMPv1 para SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="717ee-116">Dá suporte à política de retransmissão do aplicativo e fornece suporte à execução de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="717ee-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="717ee-117">Para obter mais informações, consulte [o banco de dados WinSNMP](the-winsnmp-database.md) e [sobre a retransmissão](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="717ee-118">Fornece suporte à tradução de contexto e entidade para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="717ee-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="717ee-119">Para obter mais informações, consulte [o banco de dados WinSNMP](the-winsnmp-database.md) e [definindo o modo de tradução de entidade e contexto](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="717ee-120">Para obter informações adicionais sobre a relação entre um aplicativo WinSNMP e a implementação, consulte [conceitos de gerenciamento de dados de WinSNMP](winsnmp-data-management-concepts.md) e sessões de [WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="717ee-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




