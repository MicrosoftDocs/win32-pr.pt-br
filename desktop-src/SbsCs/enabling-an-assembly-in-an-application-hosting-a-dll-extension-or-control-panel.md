---
description: Se o seu aplicativo hospedar uma DLL, extensão, plug-in ou painel de controle de terceiros, convém habilitar um assembly em seu aplicativo&\# 8212; sem habilitar também esse assembly para os componentes hospedados.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Habilitando um assembly em um aplicativo que hospeda uma DLL, extensão ou painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748875"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="c30b3-103">Habilitando um assembly em um aplicativo que hospeda uma DLL, extensão ou painel de controle</span><span class="sxs-lookup"><span data-stu-id="c30b3-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="c30b3-104">Se o seu aplicativo hospedar uma DLL, extensão, plug-in ou painel de controle de terceiros, convém habilitar um assembly em seu aplicativo — sem habilitar também esse assembly para os componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="c30b3-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="c30b3-105">Esse pode ser o caso quando um componente hospedado requer alterações de código para usar o assembly.</span><span class="sxs-lookup"><span data-stu-id="c30b3-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="c30b3-106">Como desenvolvedor do aplicativo, talvez você não consiga fazer alterações nesses componentes de terceiros.</span><span class="sxs-lookup"><span data-stu-id="c30b3-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="c30b3-107">Nesse caso, você deve seguir o procedimento descrito nesta seção para que seu aplicativo possa usar o assembly sem afetar os componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="c30b3-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="c30b3-108">Para habilitar um assembly em um aplicativo sem afetar DLLs hospedadas, extensões, plug-ins ou painéis de controle, um manifesto que descreve a dependência do aplicativo no assembly deve ser incluído no aplicativo como um recurso.</span><span class="sxs-lookup"><span data-stu-id="c30b3-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="c30b3-109">Os componentes hospedados que não estão sendo habilitados com o assembly não devem incluir manifestos que descrevam essa dependência.</span><span class="sxs-lookup"><span data-stu-id="c30b3-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="c30b3-110">Para habilitar um assembly em um aplicativo e suas DLLs hospedadas, extensões, plug-ins ou painéis de controle, inclua manifestos como recursos no aplicativo e em seus componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="c30b3-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="c30b3-111">Os manifestos incluídos no aplicativo e nos componentes hospedados devem descrever uma dependência no assembly.</span><span class="sxs-lookup"><span data-stu-id="c30b3-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="c30b3-112">Normalmente, o desenvolvedor do aplicativo adiciona um manifesto ao aplicativo e o desenvolvedor do componente hospedado adiciona um manifesto à DLL, à extensão, ao plug-in ou ao painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c30b3-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="c30b3-113">O método a seguir pode ser usado para adicionar um manifesto a um aplicativo ou a um componente hospedado que seja uma DLL, extensão, plug-in ou painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c30b3-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="c30b3-114">**Para habilitar um assembly em um aplicativo ou componente hospedado.**</span><span class="sxs-lookup"><span data-stu-id="c30b3-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="c30b3-115">Crie um manifesto que descreva a dependência do aplicativo ou da extensão no assembly.</span><span class="sxs-lookup"><span data-stu-id="c30b3-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="c30b3-116">Por exemplo, o manifesto para "YourApplication" pode ser criado copiando o exemplo de manifesto a seguir e substituindo os valores corretos para **AssemblyIdentity**, **ProcessorArchitecture** e **Description**.</span><span class="sxs-lookup"><span data-stu-id="c30b3-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="c30b3-117">Defina o valor de **ProcessorArchitecture** como x86 se estiver compilando em uma plataforma de 32 bits e para IA64 se estiver compilando em uma plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c30b3-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="c30b3-118">O elemento **Description** contém uma descrição de opção do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c30b3-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="c30b3-119">Para obter mais informações sobre o formato do manifesto, consulte [manifestos do aplicativo](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="c30b3-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="c30b3-120">Crie um recurso no aplicativo ou extensão do tipo ID de \_ manifesto RT 2.</span><span class="sxs-lookup"><span data-stu-id="c30b3-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="c30b3-121">Por exemplo, se o nome do aplicativo for YourApp, o aplicativo deverá conter o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c30b3-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="c30b3-122">Compile o aplicativo com o sinalizador habilitado para reconhecimento de-DISOLATION \_ \_ ou insira essa instrução antes de \# incluir a instrução "Windows. h".</span><span class="sxs-lookup"><span data-stu-id="c30b3-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="c30b3-123">No caso de um aplicativo com vários módulos, o \_ sinalizador habilitado para reconhecimento de DISOLATION \_ é necessário em todos os módulos.</span><span class="sxs-lookup"><span data-stu-id="c30b3-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="c30b3-124">Teste para garantir que os assemblies usados pelo aplicativo funcionem corretamente no aplicativo e no componente hospedado.</span><span class="sxs-lookup"><span data-stu-id="c30b3-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="c30b3-125">Para obter mais informações sobre como adicionar um assembly a aplicativos sem extensões, consulte [habilitando um assembly em um aplicativo sem extensões](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c30b3-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



