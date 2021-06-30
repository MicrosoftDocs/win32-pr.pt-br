---
title: Habilitar estilos visuais
description: Este tópico explica como configurar seu aplicativo para garantir que controles comuns sejam exibidos no estilo visual preferido do usuário.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102165"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="50c46-103">Habilitar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="50c46-103">Enabling Visual Styles</span></span>

<span data-ttu-id="50c46-104">Este tópico explica como configurar seu aplicativo para garantir que controles comuns sejam exibidos no estilo visual preferido do usuário.</span><span class="sxs-lookup"><span data-stu-id="50c46-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="50c46-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="50c46-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="50c46-106">Usando manifestos ou diretivas para garantir que estilos visuais possam ser aplicados a aplicativos</span><span class="sxs-lookup"><span data-stu-id="50c46-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="50c46-107">Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão</span><span class="sxs-lookup"><span data-stu-id="50c46-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="50c46-108">Usando o ComCtl32 versão 6 no Painel de Controle ou uma DLL que é executado por RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="50c46-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="50c46-109">Adicionando suporte de estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo</span><span class="sxs-lookup"><span data-stu-id="50c46-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="50c46-110">Como desligar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="50c46-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="50c46-111">Usando estilos visuais com conteúdo HTML</span><span class="sxs-lookup"><span data-stu-id="50c46-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="50c46-112">Quando estilos visuais não são aplicados</span><span class="sxs-lookup"><span data-stu-id="50c46-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="50c46-113">Tornando seu aplicativo compatível com versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="50c46-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="50c46-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50c46-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="50c46-115">Usando manifestos ou diretivas para garantir que estilos visuais possam ser aplicados a aplicativos</span><span class="sxs-lookup"><span data-stu-id="50c46-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="50c46-116">Para permitir que seu aplicativo use estilos visuais, você deve usar ComCtl32.dll versão 6 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="50c46-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="50c46-117">Como a versão 6 não é redistribuível, ela está disponível somente quando seu aplicativo está em execução em uma versão do Windows que o contém.</span><span class="sxs-lookup"><span data-stu-id="50c46-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="50c46-118">O Windows vem com as versões 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="50c46-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="50c46-119">ComCtl32.dll versão 6 contém os controles de usuário e os controles comuns.</span><span class="sxs-lookup"><span data-stu-id="50c46-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="50c46-120">Por padrão, os aplicativos usam os controles de usuário definidos User32.dll e os controles comuns definidos ComCtl32.dll versão 5.</span><span class="sxs-lookup"><span data-stu-id="50c46-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="50c46-121">Para ver uma lista de versões de DLL e suas plataformas de distribuição, consulte [Versões de Controle Comum](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="50c46-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="50c46-122">Se você quiser que seu aplicativo use estilos visuais, deverá adicionar um manifesto do aplicativo ou uma diretiva do compilador que indica que ComCtl32.dll versão 6 deve ser usada se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="50c46-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="50c46-123">Um manifesto do aplicativo permite que um aplicativo especifique quais versões de um assembly ele requer.</span><span class="sxs-lookup"><span data-stu-id="50c46-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="50c46-124">No Microsoft Win32, um assembly é um conjunto de DLLs e uma lista de objetos com controle de versão contidos nessas DLLs.</span><span class="sxs-lookup"><span data-stu-id="50c46-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="50c46-125">Os manifestos são gravados em XML.</span><span class="sxs-lookup"><span data-stu-id="50c46-125">Manifests are written in XML.</span></span> <span data-ttu-id="50c46-126">O nome do arquivo de manifesto do aplicativo é o nome do executável seguido pela extensão de nome de arquivo .manifest; por exemplo, MyApp.exe.manifest.</span><span class="sxs-lookup"><span data-stu-id="50c46-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="50c46-127">O manifesto de exemplo a seguir mostra que a primeira seção descreve o manifesto em si.</span><span class="sxs-lookup"><span data-stu-id="50c46-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="50c46-128">A tabela a seguir mostra os atributos definidos pelo **elemento assemblyIdentity** na seção de descrição do manifesto.</span><span class="sxs-lookup"><span data-stu-id="50c46-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="50c46-129">Atributo</span><span class="sxs-lookup"><span data-stu-id="50c46-129">Attribute</span></span>             | <span data-ttu-id="50c46-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="50c46-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c46-131">version</span><span class="sxs-lookup"><span data-stu-id="50c46-131">version</span></span>               | <span data-ttu-id="50c46-132">Versão do manifesto.</span><span class="sxs-lookup"><span data-stu-id="50c46-132">Version of the manifest.</span></span> <span data-ttu-id="50c46-133">A versão deve estar no formato major.minor.revision.build (ou seja, n.n.n.n.n, em que n <=65535).</span><span class="sxs-lookup"><span data-stu-id="50c46-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="50c46-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="50c46-134">processorArchitecture</span></span> | <span data-ttu-id="50c46-135">Processador para o qual seu aplicativo é desenvolvido.</span><span class="sxs-lookup"><span data-stu-id="50c46-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="50c46-136">name</span><span class="sxs-lookup"><span data-stu-id="50c46-136">name</span></span>                  | <span data-ttu-id="50c46-137">Inclui nome da empresa, nome do produto e nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50c46-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="50c46-138">type</span><span class="sxs-lookup"><span data-stu-id="50c46-138">type</span></span>                  | <span data-ttu-id="50c46-139">Tipo de aplicativo, como Win32.</span><span class="sxs-lookup"><span data-stu-id="50c46-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="50c46-140">O manifesto de exemplo também fornece uma descrição do aplicativo e especifica as dependências do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50c46-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="50c46-141">A tabela a seguir mostra os atributos definidos pelo **elemento assemblyIdentity** na seção de dependência.</span><span class="sxs-lookup"><span data-stu-id="50c46-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="50c46-142">Atributo</span><span class="sxs-lookup"><span data-stu-id="50c46-142">Attribute</span></span>             | <span data-ttu-id="50c46-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="50c46-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="50c46-144">type</span><span class="sxs-lookup"><span data-stu-id="50c46-144">type</span></span>                  | <span data-ttu-id="50c46-145">Tipo do componente de dependência, como Win32.</span><span class="sxs-lookup"><span data-stu-id="50c46-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="50c46-146">name</span><span class="sxs-lookup"><span data-stu-id="50c46-146">name</span></span>                  | <span data-ttu-id="50c46-147">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="50c46-147">Name of the component.</span></span>                           |
| <span data-ttu-id="50c46-148">version</span><span class="sxs-lookup"><span data-stu-id="50c46-148">version</span></span>               | <span data-ttu-id="50c46-149">A versão do componente.</span><span class="sxs-lookup"><span data-stu-id="50c46-149">Version of the component.</span></span>                        |
| <span data-ttu-id="50c46-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="50c46-150">processorArchitecture</span></span> | <span data-ttu-id="50c46-151">Processador para o que o componente foi projetado.</span><span class="sxs-lookup"><span data-stu-id="50c46-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="50c46-152">Publickeytoken</span><span class="sxs-lookup"><span data-stu-id="50c46-152">publicKeyToken</span></span>        | <span data-ttu-id="50c46-153">Token de chave usado com esse componente.</span><span class="sxs-lookup"><span data-stu-id="50c46-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="50c46-154">Linguagem</span><span class="sxs-lookup"><span data-stu-id="50c46-154">language</span></span>              | <span data-ttu-id="50c46-155">Idioma do componente.</span><span class="sxs-lookup"><span data-stu-id="50c46-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="50c46-156">A seguir está um exemplo de um arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="50c46-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50c46-157">De definir a entrada **processorArchitecture** como **"X86"** se o aplicativo for destinado à plataforma Windows de 32 bits ou como **"amd64"** se seu aplicativo for destinado à plataforma Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="50c46-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="50c46-158">Você também pode especificar **" \* "**, o que garante que todas as plataformas sejam direcionadas, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="50c46-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="50c46-159">Se você estiver usando o Microsoft Visual C++ 2005 ou posterior, poderá adicionar a seguinte diretiva do compilador ao código-fonte em vez de criar manualmente um manifesto.</span><span class="sxs-lookup"><span data-stu-id="50c46-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="50c46-160">Para a capacidade de leitura, a diretiva é dividida em várias linhas aqui.</span><span class="sxs-lookup"><span data-stu-id="50c46-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="50c46-161">Os tópicos a seguir descrevem as etapas para aplicar estilos visuais a diferentes tipos de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="50c46-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="50c46-162">Observe que o formato de manifesto é o mesmo em cada caso.</span><span class="sxs-lookup"><span data-stu-id="50c46-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="50c46-163">Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão</span><span class="sxs-lookup"><span data-stu-id="50c46-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="50c46-164">A seguir estão exemplos de aplicativos que não usam extensões de terceiros.</span><span class="sxs-lookup"><span data-stu-id="50c46-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="50c46-165">Calculator</span><span class="sxs-lookup"><span data-stu-id="50c46-165">Calculator</span></span>
-   <span data-ttu-id="50c46-166">FreeCell (no Windows Vista e no Windows 7)</span><span class="sxs-lookup"><span data-stu-id="50c46-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="50c46-167">Campo de trabalho (no Windows Vista e no Windows 7)</span><span class="sxs-lookup"><span data-stu-id="50c46-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="50c46-168">Bloco de notas</span><span class="sxs-lookup"><span data-stu-id="50c46-168">Notepad</span></span>
-   <span data-ttu-id="50c46-169">Solitaire (no Windows Vista e no Windows 7)</span><span class="sxs-lookup"><span data-stu-id="50c46-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="50c46-170">**Para criar um manifesto e permitir que seu aplicativo use estilos visuais.**</span><span class="sxs-lookup"><span data-stu-id="50c46-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="50c46-171">Vincule a ComCtl32.lib e [**chame InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)</span><span class="sxs-lookup"><span data-stu-id="50c46-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="50c46-172">Adicione um arquivo chamado YourApp.exe.manifest à árvore de origem que tem o formato de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="50c46-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="50c46-173">Adicione o manifesto ao arquivo de recurso do aplicativo da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="50c46-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="50c46-174">Ao adicionar a entrada anterior ao recurso, você deve formatá-la em uma linha.</span><span class="sxs-lookup"><span data-stu-id="50c46-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="50c46-175">Como alternativa, você pode colocar o arquivo de manifesto XML no mesmo diretório que o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50c46-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="50c46-176">O sistema operacional carregará o manifesto do sistema de arquivos primeiro e, em seguida, verificará a seção de recursos do executável.</span><span class="sxs-lookup"><span data-stu-id="50c46-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="50c46-177">A versão do sistema de arquivos tem precedência.</span><span class="sxs-lookup"><span data-stu-id="50c46-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="50c46-178">Quando você criar seu aplicativo, o manifesto será adicionado como um recurso binário.</span><span class="sxs-lookup"><span data-stu-id="50c46-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="50c46-179">Usando o ComCtl32 versão 6 Painel de Controle ou uma DLL que é executado por RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="50c46-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="50c46-180">**Para criar um manifesto e permitir que seu aplicativo use estilos visuais.**</span><span class="sxs-lookup"><span data-stu-id="50c46-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="50c46-181">Vincule a ComCtl32.lib e [**chame InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)</span><span class="sxs-lookup"><span data-stu-id="50c46-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="50c46-182">Adicione um arquivo chamado YourApp.cpl.manifest à árvore de origem que tem o formato de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="50c46-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="50c46-183">Adicione o manifesto ao arquivo de recurso do aplicativo como ID de recurso 123.</span><span class="sxs-lookup"><span data-stu-id="50c46-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="50c46-184">Quando você Painel de Controle aplicativo, coloque-o na categoria apropriada.</span><span class="sxs-lookup"><span data-stu-id="50c46-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="50c46-185">Painel de Controle agora dá suporte à categorização de Painel de Controle aplicativos.</span><span class="sxs-lookup"><span data-stu-id="50c46-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="50c46-186">Isso significa que Painel de Controle aplicativos podem ser atribuídos a identificadores e separados em áreas de tarefa, como Adicionar ou Remover Programas, Aparência e Temas ou Data, Hora, Idioma e Opções Regionais.</span><span class="sxs-lookup"><span data-stu-id="50c46-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="50c46-187">Adicionando suporte de estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo</span><span class="sxs-lookup"><span data-stu-id="50c46-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="50c46-188">O suporte para estilos visuais pode ser adicionado a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo.</span><span class="sxs-lookup"><span data-stu-id="50c46-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="50c46-189">Por exemplo, use as etapas a seguir para adicionar suporte a estilos visuais para um snap-in Console de Gerenciamento Microsoft (MMC).</span><span class="sxs-lookup"><span data-stu-id="50c46-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="50c46-190">Compile o snap-in com o sinalizador -DISOLATION AWARE ENABLED ou insira a instrução a seguir antes da instrução \_ \_ include \# "windows.h".</span><span class="sxs-lookup"><span data-stu-id="50c46-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="50c46-191">Para obter mais informações sobre ISOLATION \_ AWARE \_ ENABLED, consulte [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="50c46-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="50c46-192">Inclua o arquivo de header de controle comum na origem do snap-in.</span><span class="sxs-lookup"><span data-stu-id="50c46-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="50c46-193">Adicione um arquivo chamado YourApp.manifest à árvore de origem que usa o formato de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="50c46-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="50c46-194">Adicione o manifesto ao arquivo de recurso do snap-in.</span><span class="sxs-lookup"><span data-stu-id="50c46-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="50c46-195">Consulte [Usando o ComCtl32 versão 6](/previous-versions//ms649781(v=vs.85)) em um aplicativo que usa extensões, plug-ins ou uma DLL que é trazido em um processo para obter detalhes sobre como adicionar um manifesto a um arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="50c46-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="50c46-196">Como desligar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="50c46-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="50c46-197">Você pode desativar estilos visuais para um controle ou para todos os controles em uma janela chamando a [**função SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="50c46-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="50c46-198">No exemplo anterior, *hwnd é* o handle da janela na qual desabilitar estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="50c46-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="50c46-199">Após a chamada, o controle renderiza sem estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="50c46-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="50c46-200">Usando estilos visuais com conteúdo HTML</span><span class="sxs-lookup"><span data-stu-id="50c46-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="50c46-201">As páginas HTML que modificam as folhas de estilos em cascata (CSS), como plano de fundo ou borda, não têm estilos visuais aplicados a elas.</span><span class="sxs-lookup"><span data-stu-id="50c46-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="50c46-202">Eles exibem o atributo CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="50c46-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="50c46-203">Quando especificado como parte do conteúdo, a maioria das propriedades CSS se aplica a elementos que têm estilos visuais aplicados.</span><span class="sxs-lookup"><span data-stu-id="50c46-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="50c46-204">Por padrão, os estilos visuais são aplicados a controles HTML intrínsecos em páginas exibidas no Microsoft Internet Explorer 6 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="50c46-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="50c46-205">Para desativar estilos visuais para uma página HTML, adicione uma marca META ao</span><span class="sxs-lookup"><span data-stu-id="50c46-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="50c46-206">seção.</span><span class="sxs-lookup"><span data-stu-id="50c46-206">section.</span></span> <span data-ttu-id="50c46-207">Essa técnica também se aplica ao conteúdo empacotado como HTAs (aplicativos HTML).</span><span class="sxs-lookup"><span data-stu-id="50c46-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="50c46-208">Para desativar estilos visuais, a marca META deve ser a seguinte:</span><span class="sxs-lookup"><span data-stu-id="50c46-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="50c46-209">Se a configuração do navegador e a configuração de marca não concordarem, a página não aplicará estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="50c46-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="50c46-210">Por exemplo, se a marca META estiver definida como "não" e o navegador estiver definido para habilitar estilos visuais, os estilos visuais não serão aplicados à página.</span><span class="sxs-lookup"><span data-stu-id="50c46-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="50c46-211">No entanto, se o navegador ou a marca META estiver definido como "sim" e o outro item não for especificado, os estilos visuais serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="50c46-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="50c46-212">Os estilos visuais podem alterar o layout do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="50c46-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="50c46-213">Além disso, se você definir determinados atributos em controles HTML intrínsecos, como a largura de um botão, poderá descobrir que o rótulo no botão é ilegível em determinados estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="50c46-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="50c46-214">Você deve testar completamente seu conteúdo usando estilos visuais para determinar se a aplicação de estilos visuais tem um efeito adverso em seu conteúdo e layout.</span><span class="sxs-lookup"><span data-stu-id="50c46-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="50c46-215">Quando estilos visuais não são aplicados</span><span class="sxs-lookup"><span data-stu-id="50c46-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="50c46-216">Para evitar a aplicação de estilos visuais a uma janela de nível superior, dê à janela uma região não nula (**SetWindowRgn**).</span><span class="sxs-lookup"><span data-stu-id="50c46-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="50c46-217">O sistema presume que uma janela com uma região não NULL é uma janela especializada que não usa estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="50c46-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="50c46-218">Uma janela filho associada a uma janela de nível superior não visual-styles ainda pode aplicar estilos visuais, mesmo que a janela pai não aplique.</span><span class="sxs-lookup"><span data-stu-id="50c46-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="50c46-219">Se você quiser desabilitar o uso de estilos visuais para todas as janelas em seu aplicativo, chame [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e não passe o sinalizador STAP \_ ALLOW \_ NONCLIENT.</span><span class="sxs-lookup"><span data-stu-id="50c46-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="50c46-220">Se um aplicativo não chamar **SetThemeAppProperties**, os valores de sinalizador assumidos serão STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT.</span><span class="sxs-lookup"><span data-stu-id="50c46-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="50c46-221">Os valores assumidos faz com que a área não dependente, os controles e o conteúdo da Web tenham um estilo visual aplicado.</span><span class="sxs-lookup"><span data-stu-id="50c46-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="50c46-222">Tornando seu aplicativo compatível com versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="50c46-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="50c46-223">Grande parte da arquitetura de estilo visual foi projetada para tornar mais simples continuar a enviar seu produto em versões anteriores do Windows que não suportam alterar a aparência dos controles.</span><span class="sxs-lookup"><span data-stu-id="50c46-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="50c46-224">Ao enviar um aplicativo para mais de um sistema operacional, esteja ciente do seguinte:</span><span class="sxs-lookup"><span data-stu-id="50c46-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="50c46-225">Em versões do Windows antes Windows 8, os estilos visuais estão desligados quando o alto contraste está em.</span><span class="sxs-lookup"><span data-stu-id="50c46-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="50c46-226">Para dar suporte a alto contraste, um aplicativo herdada que dá suporte a estilos visuais precisa fornecer um caminho de código separado para desenhar corretamente elementos da interface do usuário em alto contraste.</span><span class="sxs-lookup"><span data-stu-id="50c46-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="50c46-227">No Windows 8, alto contraste faz parte dos estilos visuais; No entanto, um aplicativo Windows 8 (um que inclui o GUID do Windows 8 na seção de compatibilidade do manifesto do aplicativo) ainda precisa fornecer um caminho de código separado para renderizar corretamente em alto contraste no Windows 7 anteriormente.</span><span class="sxs-lookup"><span data-stu-id="50c46-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="50c46-228">Se você usar os recursos na ComCtl32.dll versão 6, como o controle de exibição de tile ou link, deverá lidar com o caso em que esses controles não estão disponíveis no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="50c46-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="50c46-229">ComCtl32.dll versão 6 não é redistribuível.</span><span class="sxs-lookup"><span data-stu-id="50c46-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="50c46-230">Teste seu aplicativo para verificar se você não está contando com recursos do ComCtl32.dll versão 6 sem primeiro verificar a versão atual.</span><span class="sxs-lookup"><span data-stu-id="50c46-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="50c46-231">Não vincule a UxTheme.lib.</span><span class="sxs-lookup"><span data-stu-id="50c46-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="50c46-232">Escreva o código de tratamento de erros para instâncias quando os estilos visuais não funcionarem conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="50c46-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="50c46-233">Instalar o manifesto do aplicativo em versões anteriores não afetará a renderização de controles.</span><span class="sxs-lookup"><span data-stu-id="50c46-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50c46-234">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50c46-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c46-235">Estilos visuais</span><span class="sxs-lookup"><span data-stu-id="50c46-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
