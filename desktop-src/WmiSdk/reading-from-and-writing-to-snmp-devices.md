---
description: Os dispositivos SNMP podem ser acessados lendo ou escrevendo em sua instância de classe correspondente no SMIR do WMI (Repositório de Informações do Módulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lendo e escrevendo em dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0419a5fc426c183ee1eb89a957a0c2f6a210ecd9b5d4612b6c4deb4e0f775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554251"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lendo e escrevendo em dispositivos SNMP

Os dispositivos SNMP podem ser acessados lendo ou escrevendo em sua instância de classe correspondente no SMIR do WMI (Repositório de Informações do Módulo SNMP). Quando você estiver trabalhando com vários dispositivos do mesmo tipo, para eficiência, carregue os MIBs para um tipo de dispositivo SNMP no SMIR.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Selecione uma das opções a seguir para ler ou gravar de cada tipo de dispositivo SNMP atualizando as informações de contexto da instância antes de se comunicar com cada uma delas.

-   Use um nome DNS em vez do endereço IP ao referenciar um dispositivo específico.

    O exemplo a seguir mostra como usar o nome DNS para um dispositivo específico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Crie um namespace separado e associe um endereço de dispositivo ao objeto de namespace usando o qualificador de instância agentAddress para que o namespace seja permanentemente associado ao dispositivo. Nesse caso, você não precisa especificar as informações do objeto de contexto.
-   Leitura de um dispositivo SNMP.

    O exemplo a seguir executa uma operação Get em uma classe de dispositivo.

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

    O exemplo a seguir executa uma operação Definir em uma classe de dispositivo.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Classes correlacionadas são aquelas às que um determinado dispositivo SNMP é conhecido por dar suporte quando a enumeração ocorre. A correlação afeta o conjunto de classes retornadas do SMIR. A enumeração não corrigida retorna todas as classes presentes no SMIR, independentemente de o dispositivo dar suporte a elas. Para obter mais informações sobre como usar técnicas de correlação WMI, consulte Correlação de classe [SNMP WMI](wmi-snmp-class-correlation.md).

 

 



