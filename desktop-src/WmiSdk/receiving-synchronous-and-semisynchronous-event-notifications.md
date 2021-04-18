---
description: Use SWbemServices.ExecQuery para solicitar todos os eventos existentes.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Recebendo notificações de eventos síncronas e Semisynchronous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781546"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Recebendo notificações de eventos síncronas e Semisynchronous

Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para solicitar todos os eventos existentes.

O exemplo de código a seguir mostra como consultar os eventos em um log.

`Select * from Win32_NTLogEvent`

Para obter mais informações, consulte [determinando o tipo de evento a receber](determining-the-type-of-event-to-receive.md), [recebendo notificações de eventos](receiving-event-notifications.md)e [WQL (SQL para WMI)](wql-sql-for-wmi.md).

A chamada padrão para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usa a comunicação semisynchronous. O parâmetro *iFlags* tem os sinalizadores **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** definidos por padrão. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

O procedimento a seguir descreve como receber a notificação de eventos do semisynchronous usando o VBScript.

**Para receber a notificação de eventos do semisynchronous no VBScript**

1.  Crie uma consulta para o tipo de evento que você deseja receber. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

2.  Se você solicitar um tipo de evento de instância como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indique na consulta um tipo de instância de destino, por exemplo, disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Se necessário, especifique uma instância, por exemplo, o nome de um namespace ao solicitar instâncias de [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) futuras para um namespace específico.

4.  Especifique um intervalo de sondagem para Instrumentação de Gerenciamento do Windows (WMI) em uma consulta, como "dentro de 10", para sondar a cada 10 segundos. Para obter mais informações, consulte a [cláusula Within](within-clause.md).

5.  Chame [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usando a consulta.

6.  Faça um loop pela coleção que você receber.

O exemplo a seguir mostra como monitorar a inserção e a remoção de discos de uma unidade de disquete em um computador local. O script solicita \_ instâncias [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) para a instância de disco rígido do [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de unidade de disquete e sonda a cada 10 segundos para novas instâncias. Esse script é um exemplo de um consumidor de evento temporário e continua em execução até que seja interrompido no Gerenciador de tarefas ou o sistema seja reinicializado. Para obter mais informações, consulte [recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md).


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



O procedimento a seguir descreve como receber a notificação de eventos do semisynchronous usando o C++.

**Para receber a notificação de eventos do semisynchronous em C++**

1.  Configure o aplicativo com chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Como o WMI é baseado em COM, chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) é uma etapa necessária para um aplicativo WMI. Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).

2.  Determine o tipo de eventos que você deseja receber.

    O WMI dá suporte a eventos intrínsecos e extrínsecos. Um evento intrínseco é um evento predefinido pelo WMI. Um evento extrínsecos é um evento definido por um provedor de terceiros. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

3.  Registre-se para receber uma classe específica de eventos com uma chamada para o método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .

    Torne cada consulta muito específica. O objetivo do registro é registrar-se para receber apenas as notificações necessárias. Notificações que não são necessárias para processamento de desperdício e tempo de entrega.

    Você pode criar um consumidor de eventos para receber vários eventos. Por exemplo, um consumidor pode exigir notificação de eventos de modificação de instância para uma classe específica de eventos de violação de segurança e dispositivo. Nesse caso, as tarefas que um consumidor realiza ao receber um evento de modificação de instância são diferentes para os dois eventos. Portanto, o consumidor deve fazer uma chamada para [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) para registrar eventos de modificação de instância e outra chamada para **ExecNotificationQuery** para registrar eventos de violação de segurança.

    Na chamada para [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), defina o parâmetro *LFlags* como **sinalizador WBEM \_ \_ retornar \_ imediatamente** e o **sinalizador WBEM \_ \_ \_ somente para frente**. O **\_ sinalizador WBEM \_ retorna \_ imediatamente** sinaliza solicitações semisynchronous e o sinalizador **WBEM \_ \_ \_ somente encaminhar** solicita um enumerador somente encaminhamento. Para obter mais informações, consulte [chamando um método](calling-a-method.md). A função **ExecNotificationQuery** retorna um ponteiro para uma interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

4.  Sondar notificações de eventos registrados fazendo chamadas repetidas para o método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .
5.  Quando terminar, libere o enumerador que aponta para o objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

    Você pode liberar o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associado ao registro. Liberar o ponteiro de **IWbemServices** faz com que o WMI pare de entregar eventos a todos os consumidores temporários associados.

 

 
