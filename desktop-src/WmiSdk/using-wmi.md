---
description: Roteiro para usar o WMI para obter dados para scripts de cliente e aplicativos ou para fornecer dados ao WMI de um aplicativo.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Usando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475312"
---
# <a name="using-wmi"></a>Usando o WMI

Você pode usar o WMI de aplicativos cliente e scripts. Ele fornece uma infraestrutura que facilita a descoberta e a execução de tarefas de gerenciamento. Além disso, você pode adicionar ao conjunto de tarefas de gerenciamento possíveis criando seus próprios provedores WMI.

> [!Note]  
> A versão de última geração do WMI para escrever aplicativos e scripts está disponível por meio da MI (infraestrutura de gerenciamento Windows) do Windows. Para obter mais informações, consulte [Provedores de MI e clientes](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

Os seguintes tópicos são discutidos nesta seção:

-   [Obtendo dados do WMI](#obtaining-data-from-wmi)
-   [Fornecendo dados ao WMI](#providing-data-to-wmi)
-   [Tarefas importantes para o WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Obtendo dados do WMI

O procedimento a seguir descreve como obter dados do WMI escrevendo um script ou aplicativo.

**Para obter dados do WMI escrevendo um script ou aplicativo**

1.  Decida qual idioma usar. Para obter mais informações sobre scripts, consulte [Criando um script WMI](creating-a-wmi-script.md). Para obter mais informações sobre o C++, consulte [Criando um aplicativo WMI usando C++.](creating-a-wmi-application-using-c-.md) Para usar mais informações sobre C# ou WMI .NET, consulte Visão [geral do WMI .NET.](/previous-versions/)

    Você pode exibir ou manipular dados WMI em muitos idiomas. A tabela a seguir lista os tópicos que descrevem como usar os scripts e as linguagens de aplicativo para obter dados.

    

    
| Idioma do aplicativo | Tópico | 
|----------------------|-------|
| Scripts escritos na hospedagem ActiveX script da Microsoft, incluindo Visual Basic VBScript (Scripting Edition) e Perl<br /> | <a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br /> Comece com <a href="creating-a-wmi-script.md">a criação de um script WMI.</a><br /> Para exemplos de código de script, consulte <a href="wmi-tasks-for-scripts-and-applications.md">Tarefas WMI para scripts</a> e aplicativos e o Repositório de <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> do TechNet.<br /> | 
| Usando o Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Ponto de Partida com Windows PowerShell</a><br /> Cmdlets do PowerShell do WMI, como <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject.</a><br /> | 
| Visual Basic aplicativos<br /> | <a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br /> | 
| Páginas de Active Server<br /> | <a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br /> Comece com <a href="creating-active-server-pages-for-wmi.md">Criando páginas Active Server para WMI</a>.<br /> | 
| aplicativos C++<br /> | <a href="com-api-for-wmi.md">API COM para WMI</a>.<br /> Comece com <a href="creating-a-wmi-application-using-c-.md">Criando um aplicativo WMI usando exemplos</a> de aplicativo C++ e <a href="wmi-c---application-examples.md">WMI C++</a> (contém exemplos).<br /> | 
| .NET Framework aplicativos escritos em C#, Visual Basic .NET ou J #<br /> | Classes no namespace <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure.</strong></a><br /><blockquote>    [!Note]<br /><strong>System.Management era</strong> o namespace original que abordava o código gerenciado para WMI. No entanto, a tecnologia subjacente para <strong>System.Management</strong> geralmente é mais lenta do que e não é dimensionado tão bem quanto <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure.</strong></a> Dessa forma, não é recomendável que você use <strong>System.Management para</strong> novos projetos. (Para obter mais informações sobre <strong>System.Management</strong>, consulte <a href="/previous-versions/bb404655(v=vs.90)">Visão geral do WMI .NET</a>.    </blockquote><br /> | 


    

     

2.  Verifique se suas conexões com computadores remotos funcionam.

    Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)

3.  Conectar-se ao WMI em computadores remotos requer as configurações de segurança corretas, conforme explicado em [Mantendo a segurança WMI](maintaining-wmi-security.md). A tabela a seguir lista os tópicos que descrevem como definir configurações de segurança com os scripts e os idiomas do aplicativo.

    

    | Linguagem                                                      | Tópico                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Scripts em qualquer linguagem, Visual Basic aplicativos<br/> | [Definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Páginas de Active Server<br/>                                | [Configurando o IIS 5 e posterior para scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md) e definindo a segurança em [IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Depois de se conectar ao WMI, você pode obter dados por meio de consultas e enumerações.

    Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e [consultando com WQL](querying-with-wql.md).

5.  Os dados do Registro estão disponíveis por meio do WMI e você pode criar novas chaves e valores ou modificar os existentes.

    Para obter mais informações, [consulte Modificando o Registro do Sistema.](modifying-the-system-registry.md)

6.  Você pode assinar notificações de eventos por meio do WMI, temporariamente entre reinicializações do sistema ou permanentemente.

    Para obter mais informações, [consulte Monitorando eventos e](monitoring-events.md) recebendo um evento [WMI](receiving-a-wmi-event.md).

7.  Os dados do contador de desempenho para um sistema estão disponíveis por meio do WMI.

    Os contadores da biblioteca de desempenho do sistema são convertidos em classes WMI. Para obter mais informações, consulte [Monitorando dados de desempenho.](monitoring-performance-data.md)

8.  [Tarefas WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md) descreve como realizar muitas tarefas administrativas com o WMI.

## <a name="providing-data-to-wmi"></a>Fornecendo dados ao WMI

O procedimento a seguir descreve como fornecer dados ao WMI escrevendo um provedor.

**Para fornecer dados ao WMI escrevendo um provedor**

-   Decida o tipo de provedor a ser escrito.

    Não é possível escrever um provedor WMI no VBScript. No entanto, você pode usar várias outras abordagens para escrever um provedor WMI COM:

    -   Usando o Assistente de ATL do WMI Visual Studio.

        Essa abordagem cria um provedor COM nãomanagedo. Para obter mais informações, consulte [Adicionando um provedor de instância WMI](./writing-an-instance-provider.md) e [Adicionando um provedor de eventos WMI](./writing-an-event-provider.md).

    -   Usando COM diretamente em qualquer ambiente de desenvolvimento integrado.

        Essa abordagem cria um provedor COM nãomanagedo.

    -   Usando o WMI no .NET Framework para criar um provedor de código gerenciado.

        Essa abordagem cria um provedor de código gerenciado. Os provedores de código gerenciado podem ser escritos em qualquer linguagem .NET Framework, são mais simples de escrever do que os provedores COM do WMI e podem obter dados das classes baseadas em [*CIM*](gloss-c.md)do WMI, como [classes Win32.](/windows/desktop/CIMWin32Prov/win32-provider) No entanto, o .NET Framework provedor WMI tem algumas limitações. Para obter mais informações, consulte [Managing Applications Using WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   Não é [recomendável usar as classes de estrutura](wmi-c-classes.md) do provedor.

        A estrutura do provedor foi superada pelos assistentes da ATL do WMI, usando o COM diretamente ou .NET Framework provedores. Não é mais recomendável criar um provedor COM WMI com as classes de estrutura do provedor. A tabela a seguir lista os tópicos que descrevem como usar provedores COM ou .NET Framework dados.

    

    | Provedor                                                      | Tópico                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Provedor COM no mesmo processo que o WMI<br/>            | [Fornecendo dados ao WMI](providing-data-to-wmi.md)<br/>                                           |
    | Provedor desaplados COM<br/>                             | [Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework provedor em C# ou Visual Basic.NET<br/> | [Gerenciando aplicativos usando o WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Tarefas importantes para o WMI

Os tópicos a seguir fornecem informações sobre como usar o WMI para monitorar e controlar componentes corporativos.



| Tópico                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Descreve como localizar a classe e os procedimentos corretos do WMI a ser usado em scripts e aplicativos que executam tarefas comuns de administração de rede e computador, como adicionar uma nova conexão de impressora para um computador remoto ou localizar todos os hotfixes instalados em um computador.<br/>                                                                            |
| [Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | qualquer linguagem de script, como VBScript ou Perl, que funcione com ActiveX objetos pode acessar dados do WMI. os aplicativos podem acessar o wmi em C++, usando a [api COM para wmi](com-api-for-wmi.md) ou no Visual Basic, usando a[biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb e a [API de script para WMI](scripting-api-for-wmi.md).<br/> |
| [Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Descreve como scripts, aplicativos e provedores podem estabelecer conexões com o WMI em computadores remotos para obter dados ou controlar hardware e software.<br/>                                                                                                                                                                                                   |
| [Conectando-se ao WMI em um computador remoto usando Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | descreve como usar Windows PowerShell para estabelecer conexões com o WMI em computadores remotos para obter dados ou controlar hardware e software.<br/>                                                                                                                                                                                                            |
| [Eventos de monitoramento](monitoring-events.md)<br/>                                                                                           | Descreve como obter notificações de eventos criando consumidores de eventos WMI temporários ou permanentes.<br/>                                                                                                                                                                                                                                                           |
| [Fornecendo dados ao WMI](providing-data-to-wmi.md)<br/>                                                                                   | O WMI fornece dados de gerenciamento dinâmico para scripts e aplicativos de cliente ao obtê-los de provedores.<br/>                                                                                                                                                                                                                                                    |
| [Obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Descreve como acessar provedores não padrão e considerações para gravadores de provedor em sistemas de 64 bits.<br/>                                                                                                                                                                                                                                                    |



