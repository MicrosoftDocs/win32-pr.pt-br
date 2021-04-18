---
description: Se o seu aplicativo não hospedar uma DLL, uma extensão, um plug-in ou um painel de controle, você poderá usar o método descrito nesta seção para habilitar um assembly para seu aplicativo.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Habilitando um assembly em um aplicativo sem extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751825"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="71efd-103">Habilitando um assembly em um aplicativo sem extensões</span><span class="sxs-lookup"><span data-stu-id="71efd-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="71efd-104">Se o seu aplicativo não hospedar uma DLL, uma extensão, um plug-in ou um painel de controle, você poderá usar o método descrito nesta seção para habilitar um assembly para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71efd-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="71efd-105">Para obter mais informações sobre como adicionar um assembly a aplicativos com extensões, consulte [habilitando um assembly em um aplicativo que hospeda uma dll, uma extensão ou um painel de controle](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="71efd-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="71efd-106">**Para habilitar um assembly em um aplicativo sem componentes hospedados**</span><span class="sxs-lookup"><span data-stu-id="71efd-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="71efd-107">Crie um manifesto que descreva a dependência do aplicativo ou da extensão no assembly.</span><span class="sxs-lookup"><span data-stu-id="71efd-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="71efd-108">Por exemplo, o manifesto para "YourApplication" pode ser criado copiando o exemplo de manifesto a seguir e substituindo os valores corretos para **AssemblyIdentity**, **ProcessorArchitecture** e **Description**.</span><span class="sxs-lookup"><span data-stu-id="71efd-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="71efd-109">Defina o valor de **ProcessorArchitecture** como x86 se estiver compilando em uma plataforma de 32 bits e para IA64 se estiver compilando em uma plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="71efd-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="71efd-110">O elemento **Description** contém uma descrição de opção do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71efd-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="71efd-111">Para obter mais informações sobre o formato do manifesto, consulte [manifestos do aplicativo](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="71efd-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="71efd-112">Adicione o manifesto ao aplicativo como um recurso no arquivo de cabeçalho executável binário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71efd-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="71efd-113">Não é recomendável que você adicione o manifesto ao aplicativo como um arquivo de manifesto externo.</span><span class="sxs-lookup"><span data-stu-id="71efd-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="71efd-114">Para adicionar o manifesto como um recurso, crie um recurso no aplicativo do tipo ID de \_ manifesto RT 1.</span><span class="sxs-lookup"><span data-stu-id="71efd-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="71efd-115">Por exemplo, se o nome do aplicativo for YourApp, o arquivo de cabeçalho do aplicativo deverá conter o seguinte:</span><span class="sxs-lookup"><span data-stu-id="71efd-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="71efd-116">Se, em vez disso, você adicionar o manifesto como um arquivo de manifesto externo, certifique-se de que a instalação copie o arquivo de manifesto na pasta que contém o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71efd-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="71efd-117">Teste para garantir que os assemblies usados pelo aplicativo funcionem corretamente no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71efd-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



