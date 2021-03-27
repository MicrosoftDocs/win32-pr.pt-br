---
description: Use programas padrão para definir a experiência do usuário padrão.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programas padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2021
ms.locfileid: "103837526"
---
# <a name="default-programs"></a><span data-ttu-id="2d11d-103">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-103">Default Programs</span></span>

<span data-ttu-id="2d11d-104">Use **programas padrão** para definir a experiência do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="2d11d-105">Os usuários podem acessar os **programas padrão** no painel de controle ou diretamente no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="2d11d-106">Definir a ferramenta de [acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) , a experiência dos padrões primários para usuários no Windows XP, agora é uma parte dos **programas padrão**.</span><span class="sxs-lookup"><span data-stu-id="2d11d-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d11d-107">Este tópico não se aplica ao Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d11d-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="2d11d-108">A maneira como as associações de arquivo padrão funcionam alteradas no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d11d-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="2d11d-109">Para obter mais informações, consulte a seção sobre **alterações de como o Windows 10 trata os aplicativos padrão** nesta [postagem](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="2d11d-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="2d11d-110">Quando um usuário define padrões de programa usando **programas padrão**, a configuração padrão aplica-se somente a esse usuário e não a outros usuários que podem usar o mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="2d11d-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="2d11d-111">**Os programas padrão** fornecem um conjunto de APIs (preteridas no Windows 8) que permitem que fornecedores de software independentes (ISVs) incluam seus programas ou aplicativos no sistema de padrões.</span><span class="sxs-lookup"><span data-stu-id="2d11d-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="2d11d-112">O conjunto de APIs também ajuda os ISVs a gerenciar melhor seu status como padrões.</span><span class="sxs-lookup"><span data-stu-id="2d11d-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="2d11d-113">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2d11d-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2d11d-114">Introdução aos programas padrão e seu conjunto de API relacionado</span><span class="sxs-lookup"><span data-stu-id="2d11d-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="2d11d-115">Registrando um aplicativo para uso com programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="2d11d-116">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="2d11d-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="2d11d-117">Descrições de subchave e valor do registro</span><span class="sxs-lookup"><span data-stu-id="2d11d-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="2d11d-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2d11d-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="2d11d-119">Exemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="2d11d-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="2d11d-120">Tornando-se o navegador padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="2d11d-121">Interface do usuário de programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="2d11d-122">Práticas recomendadas para o uso de programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="2d11d-123">Durante a instalação</span><span class="sxs-lookup"><span data-stu-id="2d11d-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="2d11d-124">Após a instalação</span><span class="sxs-lookup"><span data-stu-id="2d11d-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="2d11d-125">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2d11d-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="2d11d-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d11d-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="2d11d-127">Introdução aos programas padrão e seu conjunto de API relacionado</span><span class="sxs-lookup"><span data-stu-id="2d11d-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="2d11d-128">Os **programas padrão** são projetados principalmente para aplicativos que usam tipos de arquivo padrão, como arquivos. mp3 ou. jpg ou protocolos padrão, como http ou mailto.</span><span class="sxs-lookup"><span data-stu-id="2d11d-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="2d11d-129">Os aplicativos que usam seus próprios protocolos proprietários e associações de arquivos normalmente não usam a funcionalidade de **programas padrão** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="2d11d-130">Depois de registrar um aplicativo para a funcionalidade de **programas padrão** , as seguintes opções e funcionalidades estão disponíveis usando o conjunto de API:</span><span class="sxs-lookup"><span data-stu-id="2d11d-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="2d11d-131">Restaure todos os padrões registrados para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="2d11d-132">Preterido para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d11d-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="2d11d-133">Restaurar um único padrão registrado para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="2d11d-134">Preterido para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d11d-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="2d11d-135">Consulta para o proprietário de um padrão específico em uma única chamada em vez de Pesquisar o registro.</span><span class="sxs-lookup"><span data-stu-id="2d11d-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="2d11d-136">Você pode consultar o padrão de uma associação de arquivo, um protocolo ou um verbo canônico do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="2d11d-137">Inicie uma interface do usuário para um aplicativo específico em que um usuário pode definir padrões individuais.</span><span class="sxs-lookup"><span data-stu-id="2d11d-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="2d11d-138">Remova todas as associações por usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-138">Remove all per-user associations.</span></span>

<span data-ttu-id="2d11d-139">**Os programas padrão** também fornecem uma interface do usuário que permite registrar um aplicativo a fim de fornecer informações adicionais ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="2d11d-140">Por exemplo, um aplicativo assinado digitalmente pode incluir uma URL para o home page do fabricante.</span><span class="sxs-lookup"><span data-stu-id="2d11d-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="2d11d-141">O uso do conjunto de APIs associado pode ajudar um aplicativo a funcionar corretamente no recurso de controle de conta de usuário (UAC) introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d11d-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="2d11d-142">No UAC, um administrador aparece no sistema como um usuário padrão, de modo que o administrador não possa, normalmente, gravar na subárvore do **\_ \_ computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="2d11d-143">Essa restrição é um recurso de segurança que impede que um processo atue como administrador sem o conhecimento do administrador.</span><span class="sxs-lookup"><span data-stu-id="2d11d-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="2d11d-144">A instalação de um programa por um usuário geralmente é executada como um processo elevado.</span><span class="sxs-lookup"><span data-stu-id="2d11d-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="2d11d-145">No entanto, as tentativas de um aplicativo para modificar os comportamentos de associação padrão em uma pós-instalação no nível do computador não serão bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="2d11d-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="2d11d-146">Em vez disso, os padrões devem ser registrados em um nível por usuário, o que impede que vários usuários substituam os padrões uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="2d11d-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="2d11d-147">A estrutura hierárquica do registro para associações de arquivo e protocolo fornece precedência para padrões por usuário em padrões de nível de máquina.</span><span class="sxs-lookup"><span data-stu-id="2d11d-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="2d11d-148">Alguns aplicativos incluem pontos em seu código que elevam temporariamente seus direitos quando eles afirmam padrões registrados no **\_ \_ computador local hKey**.</span><span class="sxs-lookup"><span data-stu-id="2d11d-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="2d11d-149">Esses aplicativos poderão apresentar resultados inesperados se outro aplicativo já estiver registrado como o padrão por usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="2d11d-150">O uso de **programas padrão** impede essa ambiguidade e garante os resultados esperados em um nível por usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="2d11d-151">Registrando um aplicativo para uso com programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="2d11d-152">Esta seção mostra as subchaves e os valores do registro necessários para registrar um aplicativo com **programas padrão**.</span><span class="sxs-lookup"><span data-stu-id="2d11d-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="2d11d-153">Ele inclui um exemplo completo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-153">It includes a full example.</span></span>

<span data-ttu-id="2d11d-154">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="2d11d-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="2d11d-155">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="2d11d-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="2d11d-156">Descrições de subchave e valor do registro</span><span class="sxs-lookup"><span data-stu-id="2d11d-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="2d11d-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2d11d-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="2d11d-158">Exemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="2d11d-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="2d11d-159">Os **programas padrão** exigem que cada aplicativo registre explicitamente as associações de arquivo, associações de MIME e protocolos para os quais o aplicativo deve ser listado como um padrão possível.</span><span class="sxs-lookup"><span data-stu-id="2d11d-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="2d11d-160">Registre as associações usando os seguintes elementos do registro, que são explicados em detalhes posteriormente neste tópico em [descrições de subchave de registro e valor](#registration-subkey-and-value-descriptions):</span><span class="sxs-lookup"><span data-stu-id="2d11d-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="2d11d-161">O exemplo a seguir mostra as entradas do registro para um navegador da Contoso fictício chamado WebBrowser:</span><span class="sxs-lookup"><span data-stu-id="2d11d-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="2d11d-162">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="2d11d-162">ProgIDs</span></span>

<span data-ttu-id="2d11d-163">Um aplicativo deve fornecer um [ProgID](fa-progids.md)específico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="2d11d-164">Certifique-se de incluir todas as informações que normalmente são gravadas na subchave padrão genérica para a extensão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="2d11d-165">Por exemplo, o player de mídia fictício do fictícia fornece as classes de software de **\_ \_ computador local de hKey locais** de aplicativo \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** subchave.</span><span class="sxs-lookup"><span data-stu-id="2d11d-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="2d11d-166">Essa subchave inclui todas as informações na subchave padrão genérica **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **. mp3** mais quaisquer informações adicionais que você deseja que o aplicativo registre.</span><span class="sxs-lookup"><span data-stu-id="2d11d-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="2d11d-167">Isso garante que, se o usuário restaurar a associação. mp3 para o Litware Player, as informações do Litware Player ficarão intactas e não foram substituídas por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="2d11d-168">(A substituição poderá ocorrer se a subchave padrão for a única fonte dessas informações.)</span><span class="sxs-lookup"><span data-stu-id="2d11d-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="2d11d-169">Quando você mapeia um ProgID para uma extensão de nome de arquivo ou protocolo, um aplicativo pode mapear um-para-um ou um para muitos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="2d11d-170">No exemplo da Contoso, ContosoHTML aponta para um único ProgID que fornece informações de ShellExecute para as extensões. htm,. html,. shtml,. XHT e. xhtml.</span><span class="sxs-lookup"><span data-stu-id="2d11d-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="2d11d-171">Como existe um ProgID diferente para cada protocolo, quando você usa protocolos, você habilita cada protocolo para ter sua própria cadeia de caracteres de execução.</span><span class="sxs-lookup"><span data-stu-id="2d11d-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="2d11d-172">Quando o tipo MIME pode ser exibido embutido em um navegador, o ProgID do tipo MIME deve conter a subchave **CLSID** que usa o CLSID (identificador de classe) do aplicativo correspondente.</span><span class="sxs-lookup"><span data-stu-id="2d11d-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="2d11d-173">Esse CLSID é usado em uma pesquisa em relação ao CLSID no banco de dados MIME que é armazenado em **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\  \\ tipo de conteúdo de **banco de dados** MIME \\ .</span><span class="sxs-lookup"><span data-stu-id="2d11d-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="2d11d-174">Se o tipo MIME não se destina a ser exibido embutido em um navegador, essa etapa poderá ser omitida.</span><span class="sxs-lookup"><span data-stu-id="2d11d-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="2d11d-175">Descrições de subchave e valor do registro</span><span class="sxs-lookup"><span data-stu-id="2d11d-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="2d11d-176">Esta seção descreve as subchaves de registro individuais e os valores usados no registro de um aplicativo com **programas padrão**, conforme ilustrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2d11d-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="2d11d-177">Funcionalidades</span><span class="sxs-lookup"><span data-stu-id="2d11d-177">Capabilities</span></span>

<span data-ttu-id="2d11d-178">A subchave **Capabilities** contém todas as informações de **programas padrão** para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="2d11d-179">O espaço reservado% ApplicationCapabilityPath% refere-se ao caminho do registro de **HKEY \_ Current \_ User** ou **HKEY \_ local \_ Machine** à subchave de **funcionalidades** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="2d11d-180">Essa subchave contém os valores significativos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d11d-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="2d11d-181">Valor</span><span class="sxs-lookup"><span data-stu-id="2d11d-181">Value</span></span>                  | <span data-ttu-id="2d11d-182">Type</span><span class="sxs-lookup"><span data-stu-id="2d11d-182">Type</span></span>                       | <span data-ttu-id="2d11d-183">Significado</span><span class="sxs-lookup"><span data-stu-id="2d11d-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d11d-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="2d11d-184">ApplicationDescription</span></span> | <span data-ttu-id="2d11d-185">REG \_ sz ou reg \_ Expand \_ sz</span><span class="sxs-lookup"><span data-stu-id="2d11d-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="2d11d-186">**Obrigatório**.</span><span class="sxs-lookup"><span data-stu-id="2d11d-186">**Required**.</span></span> <span data-ttu-id="2d11d-187">Para permitir que um usuário faça uma escolha de atribuição padrão informada, um aplicativo deve fornecer uma cadeia de caracteres que descreva os recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="2d11d-188">Embora o exemplo anterior da Contoso atribua a descrição diretamente ao valor ApplicationDescription, os aplicativos normalmente fornecem a descrição como um recurso que é inserido em um arquivo. dll para facilitar a localização.</span><span class="sxs-lookup"><span data-stu-id="2d11d-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="2d11d-189">Se ApplicationDescription não for fornecido, o aplicativo não aparecerá em listas de IU de programas padrão potenciais.</span><span class="sxs-lookup"><span data-stu-id="2d11d-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="2d11d-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2d11d-190">ApplicationName</span></span>        | <span data-ttu-id="2d11d-191">REG \_ sz ou reg \_ Expand \_ sz</span><span class="sxs-lookup"><span data-stu-id="2d11d-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="2d11d-192">**Opcional.**</span><span class="sxs-lookup"><span data-stu-id="2d11d-192">**Optional.**</span></span> <span data-ttu-id="2d11d-193">O nome pelo qual o programa aparece na interface do usuário de programas padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="2d11d-194">Se esses dados não forem fornecidos pelo aplicativo, o nome do programa executável associado ao primeiro ProgID registrado para o aplicativo será usado na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="2d11d-195">ApplicationName deve sempre corresponder ao nome registrado em [RegisteredApplications](#registeredapplications).</span><span class="sxs-lookup"><span data-stu-id="2d11d-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="2d11d-196">Você pode usar ApplicationName se desejar diferentes tipos de aplicativo, como um navegador e um cliente de email, para apontar para o mesmo arquivo executável enquanto eles aparecem como nomes diferentes.</span><span class="sxs-lookup"><span data-stu-id="2d11d-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="2d11d-197">Hidden</span><span class="sxs-lookup"><span data-stu-id="2d11d-197">Hidden</span></span>                 | <span data-ttu-id="2d11d-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2d11d-198">REG\_DWORD</span></span>                 | <span data-ttu-id="2d11d-199">**Opcional.**</span><span class="sxs-lookup"><span data-stu-id="2d11d-199">**Optional.**</span></span> <span data-ttu-id="2d11d-200">Defina esse valor como 1 para suprimir o aplicativo da lista de programas na caixa de diálogo **definir programas padrão** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="2d11d-201">Se esse valor for 0 ou não estiver presente, o aplicativo aparecerá na lista normalmente.</span><span class="sxs-lookup"><span data-stu-id="2d11d-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="2d11d-202">Associações de</span><span class="sxs-lookup"><span data-stu-id="2d11d-202">FileAssociations</span></span>

<span data-ttu-id="2d11d-203">A **subchave** FileAssociations contém associações de arquivo específicas que são reivindicadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="2d11d-204">Essas declarações são armazenadas como valores, com um valor para cada extensão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="2d11d-205">As associações apontam para um ProgID específico do aplicativo em vez de um ProgID genérico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="2d11d-206">No entanto, não é necessário que todas as associações apontem para a mesma ProgID.</span><span class="sxs-lookup"><span data-stu-id="2d11d-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="2d11d-207">MIMEAssociations</span><span class="sxs-lookup"><span data-stu-id="2d11d-207">MIMEAssociations</span></span>

<span data-ttu-id="2d11d-208">A subchave **MIMEAssociations** contém tipos MIME específicos que são reivindicados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="2d11d-209">Essas declarações são armazenadas como valores, com um valor para cada tipo de MIME.</span><span class="sxs-lookup"><span data-stu-id="2d11d-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="2d11d-210">O nome do valor para cada tipo MIME deve corresponder exatamente ao nome MIME armazenado no banco de dados MIME.</span><span class="sxs-lookup"><span data-stu-id="2d11d-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="2d11d-211">O valor também deve ser atribuído a um ProgID específico do aplicativo que contém o CLSID correspondente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="2d11d-212">Assumirá</span><span class="sxs-lookup"><span data-stu-id="2d11d-212">Startmenu</span></span>

<span data-ttu-id="2d11d-213">A subchave **assumirá** está associada às entradas de **email** e **Internet** atribuíveis ao usuário no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="2d11d-214">Um aplicativo deve ser registrado separadamente como um Contender para essas entradas.</span><span class="sxs-lookup"><span data-stu-id="2d11d-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="2d11d-215">Para obter mais informações, consulte [registrando programas com tipos de cliente](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="2d11d-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="2d11d-216">A partir do Windows 7, não há mais entradas de **Internet** e **email** no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="2d11d-217">Os dados de registro associados à entrada de **email** ainda são usados para o cliente MAPI padrão, mas os dados de registro associados à entrada da **Internet** não são usados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="2d11d-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="2d11d-218">Ao associar o registro do menu **Iniciar** de um aplicativo com seu registro de **programas padrão** , o aplicativo aparece como um padrão potencial na interface do usuário **definir associações** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="2d11d-219">Se o usuário tiver escolhido o aplicativo como o padrão e, em seguida, optar por restaurar todos os padrões do aplicativo posteriormente, o aplicativo será restaurado para a posição do menu **Iniciar** para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="2d11d-220">Para obter mais informações e uma ilustração, consulte a seção [interface do usuário de programas padrão](#default-programs-ui) mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="2d11d-221">A subchave **assumirá** tem duas entradas: StartMenuInternet e mail, que correspondem às posições canônicas de **Internet** e **email** no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="2d11d-222">Um aplicativo atribui o StartMenuInternet ou o mail a um valor igual ao nome da subchave registrada do aplicativo em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** ou **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** (conforme descrito em [registrando programas com tipos de cliente](reg-middleware-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="2d11d-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="2d11d-223">No caso da posição canônica do **email** no menu **Iniciar** , ele representa o cliente MAPI padrão e, portanto, pode ser considerado capaz de distribuir chamadas MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d11d-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="2d11d-224">No Windows 7, embora não haja mais uma posição canônica de **email** no menu **Iniciar** , essa subchave continua a ser usada para o cliente MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="2d11d-225">Um aplicativo que reivindica o padrão de email deve se registrar como um manipulador MAPI na seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="2d11d-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="2d11d-226">Se um cliente de email não puder dar suporte a MAPI, mas ainda quiser lutar para a posição canônica de **email** do menu **Iniciar** , ele poderá registrar uma linha de comando na seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="2d11d-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="2d11d-227">Além disso, em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *canôniconame* , adicione um valor padrão com o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="2d11d-228">Essas entradas permitem que o aplicativo seja iniciado a partir da posição de **email** do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="2d11d-229">Observe que as chamadas MAPI ainda são feitas no aplicativo, e que se enquadram no manipulador MAPI anterior ou falham se nenhum manipulador MAPI foi definido.</span><span class="sxs-lookup"><span data-stu-id="2d11d-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="2d11d-230">Para obter mais informações, consulte [registrando programas com tipos de cliente](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="2d11d-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="2d11d-231">UrlAssociations</span><span class="sxs-lookup"><span data-stu-id="2d11d-231">UrlAssociations</span></span>

<span data-ttu-id="2d11d-232">A subchave **UrlAssociations** contém os protocolos de URL específicos que são reivindicados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="2d11d-233">Essas declarações são armazenadas como valores, com um valor para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="2d11d-234">Cada protocolo deve apontar para um ProgID específico do aplicativo em vez de para um ProgID genérico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="2d11d-235">Conforme mencionado no exemplo da Contoso, você pode usar um ProgID diferente para cada protocolo para que cada um tenha sua própria cadeia de caracteres de execução.</span><span class="sxs-lookup"><span data-stu-id="2d11d-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="2d11d-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2d11d-236">RegisteredApplications</span></span>

<span data-ttu-id="2d11d-237">A subchave completa para **RegisteredApplications** é:</span><span class="sxs-lookup"><span data-stu-id="2d11d-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="2d11d-238">**HKEY \_ \_** RegisteredApplications de \\ **software** \\  do computador local</span><span class="sxs-lookup"><span data-stu-id="2d11d-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="2d11d-239">Essa subchave fornece ao sistema operacional o local do registro das informações de **programas padrão** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="2d11d-240">O local é armazenado como um valor cujo nome deve corresponder ao nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="2d11d-241">Exemplo de registro completo</span><span class="sxs-lookup"><span data-stu-id="2d11d-241">Full Registration Example</span></span>

<span data-ttu-id="2d11d-242">Este exemplo mostra as subchaves e os valores que são usados no registro do player de mídia da Litware fictícia.</span><span class="sxs-lookup"><span data-stu-id="2d11d-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="2d11d-243">O exemplo inclui as entradas de ProgID para mostrar como todas se encaixam.</span><span class="sxs-lookup"><span data-stu-id="2d11d-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="2d11d-244">A subchave a seguir mostra o ProgID específico do aplicativo para o tipo MIME. mp3:</span><span class="sxs-lookup"><span data-stu-id="2d11d-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="2d11d-245">Em seguida, está o ProgID específico do aplicativo que associa o programa Litware à extensão de nome de arquivo. mp3.</span><span class="sxs-lookup"><span data-stu-id="2d11d-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="2d11d-246">As entradas a seguir mostram o ProgID combinado para o tipo MIME. MPEG e a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="2d11d-247">As próximas entradas registram o programa Litware em **programas padrão** e usam ProgIDs registrados anteriormente</span><span class="sxs-lookup"><span data-stu-id="2d11d-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="2d11d-248">Por fim, este exemplo registra o local do registro de **programas padrão** Litware.</span><span class="sxs-lookup"><span data-stu-id="2d11d-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="2d11d-249">Tornando-se o navegador padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-249">Becoming the Default Browser</span></span>

<span data-ttu-id="2d11d-250">O registro do navegador deve seguir as práticas recomendadas descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2d11d-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="2d11d-251">Quando o navegador é instalado, o Windows pode apresentar ao usuário uma notificação do sistema por meio da qual o usuário pode selecionar o navegador como o padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="2d11d-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="2d11d-252">Essa notificação é mostrada quando essas condições são atendidas:</span><span class="sxs-lookup"><span data-stu-id="2d11d-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="2d11d-253">O instalador do navegador chama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) com o **sinalizador \_ assocchanged do SHCNE** para informar ao Windows que novos manipuladores de protocolo foram registrados.</span><span class="sxs-lookup"><span data-stu-id="2d11d-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="2d11d-254">O Windows detecta que um ou mais novos aplicativos foram registrados para lidar com os protocolos http://e https://, e o usuário ainda não foi notificado.</span><span class="sxs-lookup"><span data-stu-id="2d11d-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="2d11d-255">Em outras palavras, nenhum dos itens a seguir foi mostrado ao usuário: uma notificação do sistema anuncia o aplicativo, um submenu OpenWith que contém o aplicativo ou a página do painel de controle definir padrões do usuário (SUD) para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="2d11d-256">O exemplo a seguir mostra o código de registro recomendado que o instalador do navegador deve executar depois de gravar suas chaves de registro.</span><span class="sxs-lookup"><span data-stu-id="2d11d-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="2d11d-257">O [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primeiro notifica o sistema de que novas opções de associação estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2d11d-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="2d11d-258">A chamada **SHChangeNotify** é necessária para garantir o funcionamento adequado dos padrões do sistema.</span><span class="sxs-lookup"><span data-stu-id="2d11d-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="2d11d-259">Em seguida, uma instrução [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) permite que os processos do sistema manipulem a notificação.</span><span class="sxs-lookup"><span data-stu-id="2d11d-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="2d11d-260">Se o usuário descartar ou ignorar a notificação ou submenu resultante sem fazer uma nova seleção de navegador padrão, o navegador padrão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="2d11d-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="2d11d-261">Observe que o usuário também pode alterar o navegador padrão a qualquer momento por meio de outros mecanismos, incluindo definir padrões do usuário no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="2d11d-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="2d11d-262">Interface do usuário de programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-262">Default Programs UI</span></span>

<span data-ttu-id="2d11d-263">As ilustrações nesta seção mostram a interface do usuário para **programas padrão** , como visto pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="2d11d-264">A ilustração a seguir mostra a janela principais **programas padrão** no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="2d11d-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![captura de tela da página de entrada de programas padrão](images/defaultprogramsmain.png)

<span data-ttu-id="2d11d-266">Quando um usuário escolhe a opção **definir os programas padrão** , a janela a seguir é exibida.</span><span class="sxs-lookup"><span data-stu-id="2d11d-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="2d11d-267">Os usuários podem usar essa página para atribuir um programa padrão para todos os tipos de arquivo e protocolos para os quais o programa é um padrão possível.</span><span class="sxs-lookup"><span data-stu-id="2d11d-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="2d11d-268">Conforme mostrado na ilustração a seguir, todos os programas [registrados](#registering-an-application-for-use-with-default-programs) e o ícone do programa aparecem na caixa **programas** à esquerda.</span><span class="sxs-lookup"><span data-stu-id="2d11d-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![captura de tela da página definir programas padrão](images/setyourdefaultprograms.png)

<span data-ttu-id="2d11d-270">Quando o usuário seleciona um programa da lista, o ícone do programa e o provedor são exibidos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="2d11d-271">Se a URL for inserida no certificado assinado digitalmente do programa, o programa também poderá exibir uma URL.</span><span class="sxs-lookup"><span data-stu-id="2d11d-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="2d11d-272">Os programas que não são assinados digitalmente não podem exibir uma URL.</span><span class="sxs-lookup"><span data-stu-id="2d11d-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="2d11d-273">O texto descritivo, fornecido pelo programa durante o registro, também é exibido.</span><span class="sxs-lookup"><span data-stu-id="2d11d-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="2d11d-274">Esse texto é necessário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-274">This text is required.</span></span> <span data-ttu-id="2d11d-275">Abaixo da caixa Descrição, há uma indicação de quantos padrões o programa está atualmente atribuído do número completo que está registrado para manipular.</span><span class="sxs-lookup"><span data-stu-id="2d11d-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="2d11d-276">Para atribuir ou restaurar um programa como o padrão para todos os arquivos e protocolos para os quais ele está registrado, o usuário clica na opção **definir este programa como padrão** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="2d11d-277">Para atribuir tipos de arquivo e protocolos individuais a um programa, o usuário clica na opção **escolher padrões para este programa** , que exibe um **conjunto de associações para uma** janela de programa como a mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d11d-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="2d11d-278">Recomendamos que você chame as **associações de conjunto para um programa** usando [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span><span class="sxs-lookup"><span data-stu-id="2d11d-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![captura de tela da página definir associações para um programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="2d11d-280">Práticas recomendadas para o uso de programas padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="2d11d-281">Esta seção fornece as diretrizes de práticas recomendadas para o uso de **programas padrão** ao registrar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="2d11d-282">Ele também oferece sugestões de design para a criação de um aplicativo que forneça aos usuários a funcionalidade ideal de **programas padrão** .</span><span class="sxs-lookup"><span data-stu-id="2d11d-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="2d11d-283">Durante a instalação</span><span class="sxs-lookup"><span data-stu-id="2d11d-283">During Installation</span></span>

<span data-ttu-id="2d11d-284">Além dos procedimentos de instalação normalmente praticado no Windows XP, um aplicativo baseado no Windows Vista ou em versões posteriores deve se registrar com o recurso de **programas padrão** para aproveitar sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="2d11d-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="2d11d-285">Execute a seguinte sequência de etapas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2d11d-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="2d11d-286">As etapas 1-3 correspondem às etapas que foram usadas no Windows XP; a etapa 4 foi nova no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d11d-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="2d11d-287">Instale os arquivos binários necessários.</span><span class="sxs-lookup"><span data-stu-id="2d11d-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="2d11d-288">Escreva ProgIDs para o \_ computador local hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="2d11d-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="2d11d-289">Observe que os aplicativos devem criar ProgIDs específicos do aplicativo para suas associações.</span><span class="sxs-lookup"><span data-stu-id="2d11d-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="2d11d-290">Registre o aplicativo com **programas padrão** conforme explicado anteriormente no [registro de um aplicativo para uso com programas padrão](#registering-an-application-for-use-with-default-programs).</span><span class="sxs-lookup"><span data-stu-id="2d11d-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="2d11d-291">Após a instalação</span><span class="sxs-lookup"><span data-stu-id="2d11d-291">After Installation</span></span>

<span data-ttu-id="2d11d-292">Esta seção discute como o prompt do aplicativo deve primeiro apresentar suas opções padrão para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="2d11d-293">Ele também discute como um aplicativo pode monitorar seu status como o padrão para suas possíveis associações e protocolos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="2d11d-294">Experiências da primeira execução</span><span class="sxs-lookup"><span data-stu-id="2d11d-294">First Run Experiences</span></span>

<span data-ttu-id="2d11d-295">Quando o aplicativo é executado por um usuário pela primeira vez, é recomendável que o aplicativo exiba a IU para o usuário que normalmente inclui essas duas opções:</span><span class="sxs-lookup"><span data-stu-id="2d11d-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="2d11d-296">Aceite as configurações de aplicativo padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-296">Accept the default application settings.</span></span> <span data-ttu-id="2d11d-297">Essa opção é habilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-297">This option is selected by default.</span></span>
-   <span data-ttu-id="2d11d-298">Personalize as configurações de aplicativo padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-298">Customize the default application settings.</span></span>

<span data-ttu-id="2d11d-299">Antes do Windows 8, se o usuário aceitar as configurações padrão, seu aplicativo chamará [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que converte todas as associações em nível de máquina declaradas durante a instalação para as configurações por usuário para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="2d11d-300">Se o usuário decidir personalizar as configurações, seu aplicativo chamará [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para exibir a interface do usuário de associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="2d11d-301">A ilustração a seguir mostra essa janela para o player de mídia da Litware fictícia.</span><span class="sxs-lookup"><span data-stu-id="2d11d-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![captura de tela da página definir associações para um programa para Litware](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="2d11d-303">A janela Associação de arquivo mostra os padrões que o aplicativo registrou e também mostra o padrão atual para outras extensões e protocolos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="2d11d-304">Depois que o usuário terminar de personalizar seus padrões, ele clicará no botão **salvar** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="2d11d-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="2d11d-305">Se o usuário clicar em **Cancelar**, a janela será fechada sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="2d11d-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="2d11d-306">Você deve usar essa interface do usuário para seus aplicativos em vez de criar o seu próprio.</span><span class="sxs-lookup"><span data-stu-id="2d11d-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="2d11d-307">Ao fazer isso, você salva os recursos que antes eram necessários para desenvolver a interface do usuário da Associação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2d11d-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="2d11d-308">Você também garante que as associações sejam salvas corretamente.</span><span class="sxs-lookup"><span data-stu-id="2d11d-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="2d11d-309">Definir um aplicativo para verificar se ele é o padrão</span><span class="sxs-lookup"><span data-stu-id="2d11d-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="2d11d-310">Não há mais suporte para isso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d11d-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="2d11d-311">Normalmente, os aplicativos verificam se estão definidos como padrão quando são executados.</span><span class="sxs-lookup"><span data-stu-id="2d11d-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="2d11d-312">Defina seus aplicativos para fazer essa verificação chamando [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) ou [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span><span class="sxs-lookup"><span data-stu-id="2d11d-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="2d11d-313">Se o aplicativo determinar que ele não é o padrão, ele poderá apresentar a interface do usuário que pergunta se a situação atual deve ser aceita ou para tornar o aplicativo o padrão.</span><span class="sxs-lookup"><span data-stu-id="2d11d-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="2d11d-314">Sempre inclua uma caixa de seleção nesta interface do usuário que esteja selecionada por padrão e que apresente a opção para não ser solicitada novamente.</span><span class="sxs-lookup"><span data-stu-id="2d11d-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="2d11d-315">A escolha do padrão deve ser orientada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-315">The choice of default should be user driven.</span></span> <span data-ttu-id="2d11d-316">Um aplicativo nunca deve recuperar um padrão sem solicitar o usuário.</span><span class="sxs-lookup"><span data-stu-id="2d11d-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="2d11d-317">A ilustração a seguir mostra uma caixa de diálogo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="2d11d-317">The following illustration shows an example dialog box.</span></span>

![captura de tela de uma caixa de diálogo de exemplo](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="2d11d-319">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2d11d-319">Additional Resources</span></span>

-   [<span data-ttu-id="2d11d-320">**IApplicationAssociationRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d11d-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="2d11d-321">**IApplicationAssociationRegistrationUI**</span><span class="sxs-lookup"><span data-stu-id="2d11d-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="2d11d-322">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d11d-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d11d-323">Práticas recomendadas para associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="2d11d-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="2d11d-324">Cenário de exemplo de associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="2d11d-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="2d11d-325">Diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="2d11d-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="2d11d-326">Definir o acesso do programa e padrões do computador (SPAD)</span><span class="sxs-lookup"><span data-stu-id="2d11d-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
