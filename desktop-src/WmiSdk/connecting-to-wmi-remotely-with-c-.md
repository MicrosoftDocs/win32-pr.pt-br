---
description: Assim como acontece com outras linguagens, como PowerShell, VBScript ou C++, você pode usar o C# para monitorar remotamente o hardware e o software em computadores remotos.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Conectando-se ao WMI remotamente com C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9ed735a1440d124a065a9f509eac7c58b1fded9be0683e361903b9f02fc1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319434"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Conectando-se ao WMI remotamente com C #

Assim como acontece com outras linguagens, como PowerShell, VBScript ou C++, você pode usar o C# para monitorar remotamente o hardware e o software em computadores remotos. Conexões remotas para código gerenciado são realizadas por meio do namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) . (As versões anteriores do WMI usavam o namespace [System. Management](/dotnet/api/system.management) , que está incluído aqui para fins de integridade.)

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

Conectar-se remotamente usando classes no namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) usa DCOM como o mecanismo remoto subjacente. As conexões remotas do WMI devem estar em conformidade com os requisitos de segurança DCOM para representação e autenticação. Por padrão, um escopo é associado ao computador local e ao namespace do sistema "raiz \\ CIMv2". No entanto, você pode alterar o computador, o domínio e o namespace WMI que você acessa. Você também pode definir autoridade, representação, credenciais e outras opções de conexão.

**Para se conectar ao WMI remotamente com C# (Microsoft. Management. Infrastructure)**

1.  Crie uma sessão no computador remoto com uma chamada para [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).

    Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, poderá especificar o nome do computador na chamada de [criação](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) . Depois de ter o objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) retornado, você poderá fazer sua consulta WMI.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Para obter mais informações sobre como fazer consultas WMI com a API **Microsoft. Management. Infrastructure** em C#, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).

2.  Se você quiser definir opções diferentes para sua conexão, como diferentes credenciais, localidade ou níveis de representação, você precisará usar um objeto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) em sua chamada para [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).

    [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) é uma classe base para [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) e [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)). Você pode usar qualquer um para definir as opções em suas sessões WS-Man e DCOM, respectivamente. O exemplo de código a seguir descreve como usar um objeto [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) para definir o nível de representação como Impersonate.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Se você quiser definir as credenciais para a conexão, será necessário criar e adicionar um objeto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) ao seu [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).

    O exemplo de código a seguir descreve como criar uma classe [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , preenchê-la com o [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))apropriado e usá-la em uma chamada [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    Geralmente, é recomendável que você não codifique uma senha em seus aplicativos; como o exemplo de código acima indica, sempre que possível, tente consultar o usuário para obter a senha e armazená-la com segurança.

O WMI destina-se a monitorar o hardware e o software em computadores remotos. As conexões remotas para o WMI v1 são realizadas por meio do objeto [ManagementScope](/dotnet/api/system.management.managementscope) .

**Para se conectar ao WMI remotamente com C# (System. Management)**

1.  Crie um objeto [ManagementScope](/dotnet/api/system.management.managementscope) , usando o nome do computador e o caminho do WMI, e conecte-se ao seu destino com uma chamada para ManagementScope. Conexão ().

    Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, você só precisará especificar o caminho WMI. Depois de se conectar, você poderá fazer sua consulta WMI.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Para obter mais informações sobre como fazer consultas WMI com a API [System. Management](/dotnet/api/system.management) em C#, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).

2.  Se você se conectar a um computador remoto em um domínio diferente ou usar um nome de usuário e senha diferentes, deverá usar um objeto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) na chamada para o [ManagementScope](/dotnet/api/system.management.managementscope).

    O [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contém propriedades para descrever a autenticação, representação, nome de usuário, senha e outras opções de conexão. O exemplo de código a seguir descreve como usar uma [ConnectionOptions](/dotnet/api/system.management.connectionoptions) para definir o nível de representação como Impersonate.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    Em geral, é recomendável que você defina seu nível de representação para representar, a menos que seja explicitamente necessário. Além disso, tente evitar escrever seu nome e senha em código C#. (Se possível, consulte se você pode consultar o usuário para fornecê-los dinamicamente no tempo de execução.)

    Para obter mais exemplos de como definir propriedades diferentes em uma conexão WMI remota, consulte a seção exemplos da página de referência [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .

## <a name="microsoftmanagementinfrastructure-example"></a>Exemplo de Microsoft. Management. Infrastructure

O exemplo de código C# a seguir, com base na [postagem de blog a seguir no TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), descreve como usar [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) e [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) para definir credenciais em uma conexão remota.


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a>Exemplo de System. Management

O exemplo de código C# a seguir descreve uma conexão remota geral, usando os objetos System. Management.


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
