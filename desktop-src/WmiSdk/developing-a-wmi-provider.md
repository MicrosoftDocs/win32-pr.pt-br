---
description: Um provedor é um objeto de Component Object Model (COM) que atua como um intermediário entre o WMI e um objeto gerenciado.
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: Desenvolvendo um provedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9249c251f75f08f9e5142e70a507b0dced8f91df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812078"
---
# <a name="developing-a-wmi-provider"></a>Desenvolvendo um provedor WMI

Um provedor é um objeto de Component Object Model (COM) que atua como um intermediário entre o WMI e um objeto gerenciado. Por exemplo, quando um aplicativo ou script solicita dados de disco usando a classe do [**\_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) do WMI Win32, os dados são obtidos dinamicamente por meio do [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider)pré-instalado.

Se você quiser fornecer dados por meio do WMI para outros aplicativos, poderá criar um provedor de código não gerenciado escrevendo um servidor COM ou por meio de **assistentes WMI ATL** no Visual Studio. Você pode escrever um provedor de código gerenciado usando o WMI na .NET Framework. Os tópicos nesta seção descrevem o processo de gravação de um provedor COM não gerenciado.

> [!Note]  
> Para garantir que todas as suas definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e for reiniciado, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) no seu arquivo formato MOF (MOF).

 

Um provedor consiste em classes definidas no esquema [*formato MOF (MOF)*](gloss-m.md) e em um arquivo dll que executa as funções do provedor. Por exemplo, o MOF que define as classes do provedor Win32 é CIMWin32. mof e a DLL é CIMWin32.dll, ambos são encontrados em% windir% \\ System32 \\ WBEM.

O esquema MOF para o provedor pode conter vários tipos de provedor. Por exemplo, o [provedor de log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) tem instância, método e tipos de provedor de eventos em um arquivo MOF chamado Ntevt. mof. É recomendável que todas as classes e o esquema de registro para provedores relacionados sejam montados em um arquivo, em vez de criar um arquivo por classe.

Além de usar provedores pré-instalados, você pode criar seu próprio provedor para fornecer informações sobre um dispositivo de hardware ou as operações do software.

A tabela a seguir lista as tarefas básicas que criam um provedor.



| Tarefa                                                                                                                                                            | Descrição                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)                                                              | Desenvolva um modelo para as entidades que você deseja gerenciar por meio do WMI e crie um arquivo formato MOF (MOF) para descrever o esquema.<br/> |
| [Fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | Crie o provedor mais básico que está acoplado ao WMI.<br/>                                                                                |
| [Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md)                                                                    | Inclua o provedor como um componente em um aplicativo se ele não for executado o tempo todo.<br/>                                         |
| [Registrando um provedor](registering-a-provider.md)                                                                                                            | Registre o provedor com com e WMI.<br/>                                                                                               |
| [Inicializando um provedor](initializing-a-provider.md)                                                                                                          | Implemente as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .<br/>   |
| [Fazendo chamadas para o WMI](making-calls-to-wmi.md)                                                                                                                  | Chamar interfaces WMI de um provedor.<br/>                                                                                                  |
| [Representando um cliente](impersonating-a-client.md)                                                                                                            | Defina a segurança para acessar um aplicativo cliente.<br/>                                                                                          |
| [Atualizando um provedor](updating-a-provider.md)                                                                                                                  | Melhore o provedor conforme necessário.<br/>                                                                                                       |
| [Descarregando um provedor](unloading-a-provider.md)                                                                                                                | Remova o provedor da memória durante o desligamento ou quando o provedor estiver ocioso.<br/>                                                         |
| [Depurando provedores](debugging-providers.md) e [configuração de provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md) | Depure seu provedor usando os recursos fornecidos pelo WMI.<br/>                                                                                 |
| [Obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | Avalie se você precisa de um provedor de compatibilidade de aplicativos de 32 bits ou se o provedor de 64 bits pode fornecer dados para ambos os clientes.<br/>      |



 

Os tópicos a seguir discutem as etapas necessárias para escrever diferentes tipos de provedores:

-   [Gravando um provedor de instância](writing-an-instance-provider.md)
-   [Escrevendo um provedor de métodos](writing-a-method-provider.md)
-   [Escrevendo um provedor de eventos](writing-an-event-provider.md)
-   [Escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md)
-   [Escrevendo um provedor de classe](writing-a-class-provider.md)
-   [Gravando um provedor de propriedades](writing-a-property-provider.md)
-   [Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

 

