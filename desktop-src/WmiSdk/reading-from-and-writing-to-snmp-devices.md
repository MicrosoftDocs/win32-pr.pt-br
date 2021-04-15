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
# <a name="reading-from-and-writing-to-snmp-devices"></a>Leitura e gravação em dispositivos SNMP

Os dispositivos SNMP podem ser acessados lendo ou gravando em sua instância de classe correspondente no WMI SMIR (repositório de informações do módulo SNMP). Quando você estiver trabalhando com vários dispositivos do mesmo tipo, para eficiência, carregue os MIBs para um tipo de dispositivo SNMP no SMIR.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Selecione uma das opções a seguir para ler ou gravar de cada tipo de dispositivo SNMP atualizando as informações de contexto da instância antes de se comunicar com cada uma delas.

-   Use um nome DNS em vez do endereço IP ao fazer referência a um dispositivo específico.

    O exemplo a seguir mostra como usar o nome DNS para um dispositivo específico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Crie um namespace separado e associe um endereço de dispositivo ao objeto de namespace usando o qualificador de instância AgentAddress para que o namespace seja vinculado permanentemente ao dispositivo. Nesse caso, você não precisa especificar as informações do objeto de contexto.
-   Ler de um dispositivo SNMP.

    O exemplo a seguir executa uma operação get em uma classe de dispositivo.

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

    

-   Gravar em um dispositivo SNMP.

    O exemplo a seguir executa uma operação set em uma classe de dispositivo.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

As classes correlacionadas são aquelas para as quais um determinado dispositivo SNMP tem suporte quando ocorre a enumeração. A correlação afeta o conjunto de classes retornadas do SMIR. A enumeração não correlacionada retorna todas as classes presentes no SMIR, independentemente de o dispositivo dar suporte a elas. Para obter mais informações sobre como usar técnicas de correlação do WMI, consulte [correlação de classes SNMP WMI](wmi-snmp-class-correlation.md).

 

 



