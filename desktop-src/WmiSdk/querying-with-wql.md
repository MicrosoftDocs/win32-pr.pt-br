---
description: O linguagem WQL (WQL) é um subconjunto de linguagem SQL padrão de American National Standards Institute (ANSI SQL) com pequenas alterações semânticas para dar suporte ao WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Consultando com WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783792"
---
# <a name="querying-with-wql"></a>Consultando com WQL

O linguagem WQL (WQL) é um subconjunto de linguagem SQL padrão de American National Standards Institute (ANSI SQL) com pequenas alterações semânticas para dar suporte ao WMI.

Para obter uma lista completa de palavras-chave WQL com suporte, consulte [WQL (SQL para WMI)](wql-sql-for-wmi.md). Usar palavras-chave SQL para nomes de objeto ou propriedade pode restringir a análise de uma consulta. As seguintes palavras-chave SQL são restritas: **NULL**, **true** e **false**.

> [!Note]  
> Há limites para o número de palavras-chave AND e OR que podem ser usadas em consultas WQL. Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** . O limite de palavras-chave WQL depende da complexidade da consulta.

 

As consultas podem usar a cláusula **Where** para extensão e personalização, embora não seja necessário. A cláusula **Where** é composta de uma propriedade ou palavra-chave, um operador e uma constante. Todas as cláusulas **Where** devem especificar um dos operadores predefinidos que são incluídos na WQL. Para obter mais informações sobre a sintaxe, consulte a [cláusula WHERE](where-clause.md). Para obter mais informações sobre operadores WQL válidos, consulte [operadores WQL](wql-operators.md).

Assim como acontece com outras cadeias de caracteres de consulta SQL, você pode escapar suas consultas.

> [!Note]  
> O WQL não dá suporte a consultas ou associações de namespace cruzado. Você não pode consultar todas as instâncias de uma classe especificada que reside em todos os namespaces no computador de destino.

 

O WQL dá suporte aos seguintes tipos de consultas:

-   Consultas de dados

    As consultas de dados são usadas para recuperar instâncias de classe e associações de dados. Eles são o tipo de consulta mais comumente usado em aplicativos e scripts do WMI. Para obter mais informações sobre a sintaxe de consultas de dados, consulte [solicitando dados de instância de classe](requesting-class-instance-data.md). Para obter mais informações sobre associações, consulte [declarando uma classe de associação](declaring-an-association-class.md).

    > [!Note]  
    > WQL não oferece suporte a consultas de tipos de dataArray.

     

    O exemplo de consulta de dados a seguir solicita o arquivo de log de eventos chamado "Application" de todas as instâncias do [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Consultas de evento

    Os consumidores usam consultas de eventos para se registrar para receber notificações de eventos. Provedores de eventos usam consultas de eventos para se registrar para dar suporte a um ou mais eventos. Para obter mais informações sobre consultas de eventos, consulte [recebendo notificações de eventos](receiving-event-notifications.md).

    O seguinte exemplo de consulta de evento por um consumidor de evento temporário solicita notificação quando uma nova instância de uma classe derivada do [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) é criada.

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   Consultas de esquema

    As consultas de esquema são usadas para recuperar definições de classe (em vez de instâncias de classe) e associações de esquema. Provedores de classe usam consultas de esquema para especificar as classes que dão suporte ao se registrarem. Para obter mais informações sobre consultas de esquema, consulte [recuperando definições de classe](retrieving-class-definitions.md).

    O exemplo de consulta de esquema a seguir mostra a sintaxe especial.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de data e hora do WMI](date-and-time-format.md)
</dt> </dl>

 

 
