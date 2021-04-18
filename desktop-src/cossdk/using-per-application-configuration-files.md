---
description: Usando arquivos de configuração Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Usando arquivos de configuração Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784977"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="f6933-103">Usando arquivos de configuração Per-Application</span><span class="sxs-lookup"><span data-stu-id="f6933-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="f6933-104">O uso de arquivos de configuração do COM+ por aplicativo requer as seguintes etapas básicas:</span><span class="sxs-lookup"><span data-stu-id="f6933-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="f6933-105">Configure um diretório raiz do aplicativo para um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="f6933-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="f6933-106">Crie aplicativos. manifest e application.config arquivos no diretório raiz do aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="f6933-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="f6933-107">Arquivos de configuração por aplicativo só estão disponíveis a partir do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f6933-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="f6933-108">**Para usar um arquivo de configuração por aplicativo**</span><span class="sxs-lookup"><span data-stu-id="f6933-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="f6933-109">Crie uma biblioteca de classes .NET, com uma referência ao assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="f6933-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="f6933-110">A biblioteca de classes deve conter o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="f6933-110">The class library should contain the following code:</span></span>

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    <span data-ttu-id="f6933-111">Observe que "ConfigData1" é um exemplo de nome de configuração.</span><span class="sxs-lookup"><span data-stu-id="f6933-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="f6933-112">Você pode substituir isso pelo nome da configuração de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="f6933-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="f6933-113">Crie um aplicativo COM+ vazio.</span><span class="sxs-lookup"><span data-stu-id="f6933-113">Create an empty COM+ application.</span></span> <span data-ttu-id="f6933-114">Para obter instruções sobre como fazer isso, consulte [criando um novo aplicativo com+](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="f6933-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="f6933-115">Instale a biblioteca de classes que você criou no aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="f6933-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="f6933-116">Para obter instruções sobre como fazer isso, consulte [instalando novos componentes](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="f6933-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="f6933-117">Na ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ que você criou e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f6933-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="f6933-118">Na caixa de diálogo **Propriedades** , selecione a guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="f6933-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="f6933-119">Verifique se o **tipo de ativação** está definido como **aplicativo de servidor**.</span><span class="sxs-lookup"><span data-stu-id="f6933-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="f6933-120">Na caixa de texto **diretório raiz do aplicativo** , insira o caminho ou navegue até o diretório no qual você deseja armazenar os arquivos de configuração do aplicativo para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6933-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="f6933-121">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6933-121">Click **OK**.</span></span>

    <span data-ttu-id="f6933-122">Observe que você também pode especificar o diretório raiz do aplicativo COM+ por meio da Propriedade ApplicationDirectory da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f6933-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="f6933-123">Para obter mais informações, consulte [**aplicativos**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="f6933-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="f6933-124">No diretório que você escolheu para armazenar os arquivos de configuração do aplicativo, crie um arquivo chamado *Application*. manifest.</span><span class="sxs-lookup"><span data-stu-id="f6933-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="f6933-125">Com um editor de texto, adicione o seguinte texto a este arquivo:</span><span class="sxs-lookup"><span data-stu-id="f6933-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="f6933-126">No mesmo diretório, crie um arquivo chamado *Application*. config. Com um editor de texto, adicione o seguinte texto a este arquivo:</span><span class="sxs-lookup"><span data-stu-id="f6933-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="f6933-127">Observe que esse arquivo de configuração é apenas um exemplo.</span><span class="sxs-lookup"><span data-stu-id="f6933-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="f6933-128">Você pode criar várias chaves com nomes e valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="f6933-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="f6933-129">No entanto, observe que "ConfigData1" corresponde ao nome da configuração usado na biblioteca de classes criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f6933-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="f6933-130">Crie um aplicativo de console .NET, com uma referência à biblioteca de classes .NET criada anteriormente e uma referência ao assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="f6933-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="f6933-131">O aplicativo de console deve conter o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="f6933-131">The console application should contain the following code:</span></span>
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

<span data-ttu-id="f6933-132">Execute o aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="f6933-132">Run the console application.</span></span> <span data-ttu-id="f6933-133">A saída deverá ser como a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f6933-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



