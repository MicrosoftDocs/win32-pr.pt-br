---
description: Roteiro para usar o WMI para obter dados para scripts e aplicativos de cliente ou para fornecer dados para o WMI de um aplicativo.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Usando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31878b41de0f44a70c31c2134f0a611a9309a321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091782"
---
# <a name="using-wmi"></a>Usando o WMI

Você pode usar o WMI de scripts e aplicativos cliente. Ele fornece uma infraestrutura que facilita a descoberta e a execução de tarefas de gerenciamento. Além disso, você pode adicionar ao conjunto de tarefas de gerenciamento possíveis criando seus próprios provedores de WMI.

> [!Note]  
> A versão de próxima geração do WMI para a gravação de aplicativos e scripts está disponível por meio da MI (infraestrutura de gerenciamento do Windows). Para obter mais informações, consulte [clientes e provedores de mi](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

Os seguintes tópicos são discutidos nesta seção:

-   [Obtendo dados do WMI](#obtaining-data-from-wmi)
-   [Fornecendo dados ao WMI](#providing-data-to-wmi)
-   [Tarefas importantes para o WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Obtendo dados do WMI

O procedimento a seguir descreve como obter dados do WMI escrevendo um script ou aplicativo.

**Para obter dados do WMI escrevendo um script ou aplicativo**

1.  Decida qual idioma usar. Para obter mais informações sobre scripts, consulte [criando um script WMI](creating-a-wmi-script.md). Para obter mais informações sobre C++, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md). Para usar mais informações sobre C# ou WMI .NET, consulte [visão geral do WMI .net](/previous-versions/).

    Você pode exibir ou manipular dados do WMI em vários idiomas. A tabela a seguir lista os tópicos que descrevem como usar os scripts e linguagens de aplicativo para obter dados.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Idioma do aplicativo</th>
    <th>Tópico</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Scripts escritos em Hospedagem de script do Microsoft ActiveX, incluindo Visual Basic Scripting Edition (VBScript) e Perl<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br/> Comece com <a href="creating-a-wmi-script.md">a criação de um script WMI</a>.<br/> Para obter exemplos de código de script, consulte <a href="wmi-tasks-for-scripts-and-applications.md">tarefas WMI para scripts e aplicativos</a> e o repositório de scripts do TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Windows PowerShell<br/></td>
    <td><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Introdução com o Windows PowerShell</a><br/> Cmdlets do PowerShell do WMI, como <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>Visual Basic aplicativos<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br/></td>
    </tr>
    <tr class="even">
    <td>Páginas de Active Server<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de script para WMI</a>.<br/> Comece com a <a href="creating-active-server-pages-for-wmi.md">criação de páginas Active Server para o WMI</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>aplicativos C++<br/></td>
    <td><a href="com-api-for-wmi.md">API com para WMI</a>.<br/> Comece com <a href="creating-a-wmi-application-using-c-.md">a criação de um aplicativo WMI usando</a> os exemplos de aplicativo C++ e <a href="wmi-c---application-examples.md">WMI c++</a> (contém exemplos).<br/></td>
    </tr>
    <tr class="even">
    <td>.NET Framework aplicativos escritos em C#, Visual Basic .NET ou J #<br/></td>
    <td>Classes no namespace <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a> .<br/>
    <blockquote>
    [!Note]<br />
    <strong>System. Management</strong> foi o namespace original que abordou o código gerenciado para o WMI. No entanto, a tecnologia subjacente para <strong>System. Management</strong> é geralmente mais lenta do que e não dimensiona, bem como, <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a>. Como tal, não é recomendável que você use o <strong>System. Management</strong> para novos projetos. (Para obter mais informações sobre o <strong>System. Management</strong>, consulte <a href="/previous-versions/bb404655(v=vs.90)">visão geral do WMI .net</a>.) </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Verifique se as conexões com computadores remotos funcionam.

    Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

3.  Conectar-se ao WMI em computadores remotos requer as configurações de segurança corretas, conforme explicado em [mantendo a segurança do WMI](maintaining-wmi-security.md). A tabela a seguir lista os tópicos que descrevem como definir as configurações de segurança com os idiomas de script e de aplicativo.

    

    | Idioma                                                      | Tópico                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Scripts em qualquer linguagem, Visual Basic aplicativos<br/> | [Definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Páginas de Active Server<br/>                                | [Configurando o IIS 5 e posterior para scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md) e [definindo a segurança em IWbemServices e em outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Depois de se conectar ao WMI, você pode obter dados por meio de consultas e enumerações.

    Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e [consultando com WQL](querying-with-wql.md).

5.  Os dados do registro estão disponíveis por meio do WMI e você pode criar novas chaves e valores ou modificar os existentes.

    Para obter mais informações, consulte [modificando o registro do sistema](modifying-the-system-registry.md).

6.  Você pode assinar notificações de eventos por meio do WMI, seja temporariamente entre reinicializações do sistema ou permanentemente.

    Para obter mais informações, consulte [monitorando eventos](monitoring-events.md) e [recebendo um evento WMI](receiving-a-wmi-event.md).

7.  Os dados do contador de desempenho de um sistema estão disponíveis por meio do WMI.

    Os contadores da biblioteca de desempenho do sistema são convertidos em classes WMI. Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md).

8.  [As tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md) descrevem como fazer muitas tarefas administrativas com o WMI.

## <a name="providing-data-to-wmi"></a>Fornecendo dados ao WMI

O procedimento a seguir descreve como fornecer dados ao WMI escrevendo um provedor.

**Para fornecer dados ao WMI escrevendo um provedor**

-   Decida sobre o tipo de provedor a ser gravado.

    Você não pode gravar um provedor WMI em VBScript. No entanto, você pode usar várias outras abordagens para escrever um provedor COM WMI:

    -   Usando o assistente WMI ATL no Visual Studio.

        Essa abordagem cria um provedor COM não gerenciado. Para obter mais informações, consulte [adicionando um provedor de instância WMI](./writing-an-instance-provider.md) e [adicionando um provedor de eventos WMI](./writing-an-event-provider.md).

    -   Usando o COM diretamente em qualquer ambiente de desenvolvimento integrado.

        Essa abordagem cria um provedor COM não gerenciado.

    -   Usando o WMI no .NET Framework para criar um provedor de código gerenciado.

        Essa abordagem cria um provedor de código gerenciado. Provedores de código gerenciado podem ser escritos em qualquer linguagem de .NET Framework, são mais simples de escrever que os provedores de COM WMI e podem obter dados das classes baseadas em [*CIM*](gloss-c.md)do WMI, como [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider). No entanto, o provedor WMI .NET Framework tem algumas limitações. Para obter mais informações, consulte [Gerenciando aplicativos usando o WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   Não é recomendável usar as [classes da estrutura do provedor](wmi-c-classes.md) .

        A estrutura do provedor foi substituída pelos assistentes WMI ATL, usando o COM diretamente ou provedores de .NET Framework. Não é mais recomendável criar um provedor COM do WMI com as classes da estrutura do provedor. A tabela a seguir lista os tópicos que descrevem como usar os provedores COM ou .NET Framework.

    

    | Provedor                                                      | Tópico                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Provedor COM no mesmo processo que o WMI<br/>            | [Fornecendo dados ao WMI](providing-data-to-wmi.md)<br/>                                           |
    | Provedor dissociado COM<br/>                             | [Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md)<br/> |
    | Provedor de .NET Framework em C# ou Visual Basic.NET<br/> | [Gerenciando aplicativos usando o WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Tarefas importantes para o WMI

Os tópicos a seguir fornecem informações sobre como usar o WMI para monitorar e controlar os componentes corporativos.



| Tópico                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Descreve como encontrar a classe e os procedimentos corretos do WMI a serem usados em scripts e aplicativos que executam tarefas comuns de administração de computador e rede, como a adição de uma nova conexão de impressora para um computador remoto ou a localização de todos os hotfixes instalados em um computador.<br/>                                                                            |
| [Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | Qualquer linguagem de script, como VBScript ou Perl, que funcione com objetos ActiveX pode acessar dados do WMI. Os aplicativos podem acessar o WMI em C++, usando a [API com para WMI](com-api-for-wmi.md) ou no Visual Basic, usando a[biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb e a [API de script para WMI](scripting-api-for-wmi.md).<br/> |
| [Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Descreve como scripts, aplicativos e provedores podem estabelecer conexões com o WMI em computadores remotos para obter dados ou controlar hardware e software.<br/>                                                                                                                                                                                                   |
| [Conectando-se ao WMI em um computador remoto usando o Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Descreve como usar o Windows PowerShell para estabelecer conexões com o WMI em computadores remotos para obter dados ou controlar hardware e software.<br/>                                                                                                                                                                                                            |
| [Eventos de monitoramento](monitoring-events.md)<br/>                                                                                           | Descreve como obter notificações de eventos criando consumidores de eventos WMI temporários ou permanentes.<br/>                                                                                                                                                                                                                                                           |
| [Fornecendo dados ao WMI](providing-data-to-wmi.md)<br/>                                                                                   | O WMI fornece dados de gerenciamento dinâmico para scripts e aplicativos de cliente ao obtê-los de provedores.<br/>                                                                                                                                                                                                                                                    |
| [Obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Descreve como acessar provedores não padrão e considerações para gravadores de provedor em sistemas de 64 bits.<br/>                                                                                                                                                                                                                                                    |



