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
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011443"
---
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="b3fd5-103">Conectando-se ao WMI remotamente com C #</span><span class="sxs-lookup"><span data-stu-id="b3fd5-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="b3fd5-104">Assim como acontece com outras linguagens, como PowerShell, VBScript ou C++, você pode usar o C# para monitorar remotamente o hardware e o software em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="b3fd5-105">Conexões remotas para código gerenciado são realizadas por meio do namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="b3fd5-106">(As versões anteriores do WMI usavam o namespace [System. Management](/dotnet/api/system.management) , que está incluído aqui para fins de integridade.)</span><span class="sxs-lookup"><span data-stu-id="b3fd5-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="b3fd5-107">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="b3fd5-108">Conectar-se remotamente usando classes no namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) usa DCOM como o mecanismo remoto subjacente.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="b3fd5-109">As conexões remotas do WMI devem estar em conformidade com os requisitos de segurança DCOM para representação e autenticação.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="b3fd5-110">Por padrão, um escopo é associado ao computador local e ao namespace do sistema "raiz \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="b3fd5-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="b3fd5-111">No entanto, você pode alterar o computador, o domínio e o namespace WMI que você acessa.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="b3fd5-112">Você também pode definir autoridade, representação, credenciais e outras opções de conexão.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="b3fd5-113">**Para se conectar ao WMI remotamente com C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="b3fd5-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="b3fd5-114">Crie uma sessão no computador remoto com uma chamada para [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="b3fd5-115">Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, poderá especificar o nome do computador na chamada de [criação](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="b3fd5-116">Depois de ter o objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) retornado, você poderá fazer sua consulta WMI.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="b3fd5-117">Para obter mais informações sobre como fazer consultas WMI com a API **Microsoft. Management. Infrastructure** em C#, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="b3fd5-118">Se você quiser definir opções diferentes para sua conexão, como diferentes credenciais, localidade ou níveis de representação, você precisará usar um objeto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) em sua chamada para [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="b3fd5-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) é uma classe base para [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) e [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="b3fd5-120">Você pode usar qualquer um para definir as opções em suas sessões WS-Man e DCOM, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="b3fd5-121">O exemplo de código a seguir descreve como usar um objeto [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) para definir o nível de representação como Impersonate.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="b3fd5-122">Se você quiser definir as credenciais para a conexão, será necessário criar e adicionar um objeto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) ao seu [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="b3fd5-123">O exemplo de código a seguir descreve como criar uma classe [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , preenchê-la com o [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))apropriado e usá-la em uma chamada [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

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

    

    <span data-ttu-id="b3fd5-124">Geralmente, é recomendável que você não codifique uma senha em seus aplicativos; como o exemplo de código acima indica, sempre que possível, tente consultar o usuário para obter a senha e armazená-la com segurança.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="b3fd5-125">O WMI destina-se a monitorar o hardware e o software em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="b3fd5-126">As conexões remotas para o WMI v1 são realizadas por meio do objeto [ManagementScope](/dotnet/api/system.management.managementscope) .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="b3fd5-127">**Para se conectar ao WMI remotamente com C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="b3fd5-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="b3fd5-128">Crie um objeto [ManagementScope](/dotnet/api/system.management.managementscope) , usando o nome do computador e o caminho do WMI, e conecte-se ao seu destino com uma chamada para ManagementScope. Connect ().</span><span class="sxs-lookup"><span data-stu-id="b3fd5-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="b3fd5-129">Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, você só precisará especificar o caminho WMI.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="b3fd5-130">Depois de se conectar, você poderá fazer sua consulta WMI.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="b3fd5-131">Para obter mais informações sobre como fazer consultas WMI com a API [System. Management](/dotnet/api/system.management) em C#, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="b3fd5-132">Se você se conectar a um computador remoto em um domínio diferente ou usar um nome de usuário e senha diferentes, deverá usar um objeto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) na chamada para o [ManagementScope](/dotnet/api/system.management.managementscope).</span><span class="sxs-lookup"><span data-stu-id="b3fd5-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="b3fd5-133">O [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contém propriedades para descrever a autenticação, representação, nome de usuário, senha e outras opções de conexão.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="b3fd5-134">O exemplo de código a seguir descreve como usar uma [ConnectionOptions](/dotnet/api/system.management.connectionoptions) para definir o nível de representação como Impersonate.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="b3fd5-135">Em geral, é recomendável que você defina seu nível de representação para representar, a menos que seja explicitamente necessário.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="b3fd5-136">Além disso, tente evitar escrever seu nome e senha em código C#.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="b3fd5-137">(Se possível, consulte se você pode consultar o usuário para fornecê-los dinamicamente no tempo de execução.)</span><span class="sxs-lookup"><span data-stu-id="b3fd5-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="b3fd5-138">Para obter mais exemplos de como definir propriedades diferentes em uma conexão WMI remota, consulte a seção exemplos da página de referência [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="b3fd5-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="b3fd5-139">Exemplo de Microsoft. Management. Infrastructure</span><span class="sxs-lookup"><span data-stu-id="b3fd5-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="b3fd5-140">O exemplo de código C# a seguir, com base na [postagem de blog a seguir no TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), descreve como usar [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) e [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) para definir credenciais em uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


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



## <a name="systemmanagement-example"></a><span data-ttu-id="b3fd5-141">Exemplo de System. Management</span><span class="sxs-lookup"><span data-stu-id="b3fd5-141">System.Management Example</span></span>

<span data-ttu-id="b3fd5-142">O exemplo de código C# a seguir descreve uma conexão remota geral, usando os objetos System. Management.</span><span class="sxs-lookup"><span data-stu-id="b3fd5-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b3fd5-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3fd5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3fd5-144">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="b3fd5-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
