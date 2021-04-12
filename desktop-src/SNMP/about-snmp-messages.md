---
title: Sobre mensagens SNMP
description: O protocolo de gerenciamento de rede simples usa mensagens para se comunicar e trocar informações entre entidades SNMP remotas.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363806"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="e9091-103">Sobre mensagens SNMP</span><span class="sxs-lookup"><span data-stu-id="e9091-103">About SNMP Messages</span></span>

<span data-ttu-id="e9091-104">O protocolo de gerenciamento de rede simples usa mensagens para se comunicar e trocar informações entre entidades SNMP remotas.</span><span class="sxs-lookup"><span data-stu-id="e9091-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="e9091-105">As mensagens SNMP contêm PDUs (unidades de dados de protocolo) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante.</span><span class="sxs-lookup"><span data-stu-id="e9091-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="e9091-106">Um PDU é um pacote de dados que contém os componentes de dados SNMP (ou campos).</span><span class="sxs-lookup"><span data-stu-id="e9091-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="e9091-107">O formato de uma mensagem SNMP é o mesmo para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="e9091-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="e9091-108">No entanto, o SNMPv2C dá suporte a tipos de PDU adicionais.</span><span class="sxs-lookup"><span data-stu-id="e9091-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="e9091-109">Por exemplo, ele é compatível com o tipo de solicitação [ \_ \_ GetBulk do SNMP PDU](snmp-variable-types-and-request-pdu-types.md) , que permite que um aplicativo recupere com eficiência grandes blocos de dados de entidades de destino.</span><span class="sxs-lookup"><span data-stu-id="e9091-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




