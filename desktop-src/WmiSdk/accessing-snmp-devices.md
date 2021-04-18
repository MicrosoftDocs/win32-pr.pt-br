---
description: Permite que os aplicativos cliente acessem informações de SNMP por meio do WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Acessando dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813487"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="191d4-103">Acessando dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="191d4-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="191d4-104">O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="191d4-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="191d4-105">O [provedor SNMP](snmp-provider.md) atua como um gateway para sistemas e dispositivos que usam SNMP para gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="191d4-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="191d4-106">Somente o computador de gerenciamento ou de monitoramento deve estar executando o WMI porque ele pode ler de qualquer dispositivo habilitado para SNMP.</span><span class="sxs-lookup"><span data-stu-id="191d4-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="191d4-107">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="191d4-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="191d4-108">As variáveis de objeto de MIB (base de informações de gerenciamento) SNMP podem ser lidas e gravadas, e as interceptações SNMP podem ser mapeadas automaticamente para eventos WMI, que podem ser definidas para operações de criação, exclusão ou atualização arbitrárias para dados além das interceptações definidas pela MIB.</span><span class="sxs-lookup"><span data-stu-id="191d4-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="191d4-109">Esse recurso do WMI funciona como uma extensão dos recursos SNMP padrão.</span><span class="sxs-lookup"><span data-stu-id="191d4-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="191d4-110">Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="191d4-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="191d4-111">As ferramentas descritas nos tópicos a seguir foram projetadas para uso por scripts do Windows e programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="191d4-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="191d4-112">Recomendamos a familiaridade com o WMI, o SNMPv1 e o SNMPv2C e o conhecimento prático sobre conceitos de rede e de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="191d4-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="191d4-113">Para obter mais informações sobre como usar o WMI com SNMP, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="191d4-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 



