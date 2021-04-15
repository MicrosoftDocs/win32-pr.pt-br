---
description: Os dispositivos SNMP podem ser acessados lendo ou gravando em sua instância de classe correspondente no WMI SMIR (repositório de informações do módulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Leitura e gravação em dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505711"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="0a666-103">Leitura e gravação em dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="0a666-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="0a666-104">Os dispositivos SNMP podem ser acessados lendo ou gravando em sua instância de classe correspondente no WMI SMIR (repositório de informações do módulo SNMP).</span><span class="sxs-lookup"><span data-stu-id="0a666-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="0a666-105">Quando você estiver trabalhando com vários dispositivos do mesmo tipo, para eficiência, carregue os MIBs para um tipo de dispositivo SNMP no SMIR.</span><span class="sxs-lookup"><span data-stu-id="0a666-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="0a666-106">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0a666-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="0a666-107">Selecione uma das opções a seguir para ler ou gravar de cada tipo de dispositivo SNMP atualizando as informações de contexto da instância antes de se comunicar com cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="0a666-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="0a666-108">Use um nome DNS em vez do endereço IP ao fazer referência a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="0a666-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="0a666-109">O exemplo a seguir mostra como usar o nome DNS para um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="0a666-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="0a666-110">Crie um namespace separado e associe um endereço de dispositivo ao objeto de namespace usando o qualificador de instância AgentAddress para que o namespace seja vinculado permanentemente ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a666-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="0a666-111">Nesse caso, você não precisa especificar as informações do objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="0a666-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="0a666-112">Ler de um dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="0a666-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="0a666-113">O exemplo a seguir executa uma operação get em uma classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a666-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="0a666-114">Gravar em um dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="0a666-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="0a666-115">O exemplo a seguir executa uma operação set em uma classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a666-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="0a666-116">As classes correlacionadas são aquelas para as quais um determinado dispositivo SNMP tem suporte quando ocorre a enumeração.</span><span class="sxs-lookup"><span data-stu-id="0a666-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="0a666-117">A correlação afeta o conjunto de classes retornadas do SMIR.</span><span class="sxs-lookup"><span data-stu-id="0a666-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="0a666-118">A enumeração não correlacionada retorna todas as classes presentes no SMIR, independentemente de o dispositivo dar suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="0a666-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="0a666-119">Para obter mais informações sobre como usar técnicas de correlação do WMI, consulte [correlação de classes SNMP WMI](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="0a666-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



