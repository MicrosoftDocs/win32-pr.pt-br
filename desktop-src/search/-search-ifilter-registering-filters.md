---
description: Seu manipulador de filtro deve ser registrado. Você também pode localizar um manipulador de filtro existente para uma determinada extensão de nome de arquivo por meio do registro ou usando a interface ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrando manipuladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090079"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="1ab19-104">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="1ab19-104">Registering Filter Handlers</span></span>

<span data-ttu-id="1ab19-105">Seu manipulador de filtro deve ser registrado.</span><span class="sxs-lookup"><span data-stu-id="1ab19-105">Your filter handler must be registered.</span></span> <span data-ttu-id="1ab19-106">Você também pode localizar um manipulador de filtro existente para uma determinada extensão de nome de arquivo por meio do registro ou usando a interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .</span><span class="sxs-lookup"><span data-stu-id="1ab19-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="1ab19-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1ab19-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="1ab19-108">Registrando manipuladores de filtros para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="1ab19-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="1ab19-109">Abordagem obsoleta para registrar manipuladores de filtros</span><span class="sxs-lookup"><span data-stu-id="1ab19-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="1ab19-110">Substituindo manipuladores de filtro existentes</span><span class="sxs-lookup"><span data-stu-id="1ab19-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="1ab19-111">Localizando um manipulador de filtro para uma determinada extensão de arquivo</span><span class="sxs-lookup"><span data-stu-id="1ab19-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="1ab19-112">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1ab19-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="1ab19-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ab19-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="1ab19-114">Um manipulador de filtro é uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="1ab19-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="1ab19-115">Registrando manipuladores de filtros para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="1ab19-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="1ab19-116">Os GUIDs necessários para registrar um novo manipulador de protocolo ou para localizar um manipulador de protocolo existente são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ab19-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="1ab19-117">GUID</span><span class="sxs-lookup"><span data-stu-id="1ab19-117">GUID</span></span>                                     | <span data-ttu-id="1ab19-118">Definido pelo usuário ou aplicativo</span><span class="sxs-lookup"><span data-stu-id="1ab19-118">User or application defined</span></span> | <span data-ttu-id="1ab19-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ab19-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab19-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="1ab19-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="1ab19-121">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="1ab19-121">Application</span></span>                 | <span data-ttu-id="1ab19-122">O GUID da interface do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é uma constante de chave do registro para todos os manipuladores de filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab19-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="1ab19-123">**{PersistentHandlerGUID}**</span><span class="sxs-lookup"><span data-stu-id="1ab19-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="1ab19-124">Usuário</span><span class="sxs-lookup"><span data-stu-id="1ab19-124">User</span></span>                        | <span data-ttu-id="1ab19-125">Este é o GUID para o manipulador persistente.</span><span class="sxs-lookup"><span data-stu-id="1ab19-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="1ab19-126">**{FilterHandlerCLSID}**</span><span class="sxs-lookup"><span data-stu-id="1ab19-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="1ab19-127">Usuário</span><span class="sxs-lookup"><span data-stu-id="1ab19-127">User</span></span>                        | <span data-ttu-id="1ab19-128">Esse é o identificador de classe (CLSID) para o manipulador de filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab19-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="1ab19-129">**{ApplicationGUID}**</span><span class="sxs-lookup"><span data-stu-id="1ab19-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="1ab19-130">Usuário</span><span class="sxs-lookup"><span data-stu-id="1ab19-130">User</span></span>                        | <span data-ttu-id="1ab19-131">Esse é um GUID intermediário (agregado).</span><span class="sxs-lookup"><span data-stu-id="1ab19-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="1ab19-132">Os manipuladores de filtro devem ser registrados \_ na \_ máquina local HKEY porque SearchFilterHost.exe está em execução na conta System e, portanto, não pode acessar as chaves do registro para HKEY \_ Current \_ User para o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="1ab19-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="1ab19-133">Além disso, o grupo de usuários deve ter acesso de leitura e execução ao manipulador de filtro. dll em si porque SearchFilterHost.exe remove todos os direitos de administrador e permite somente direitos de não administrador.</span><span class="sxs-lookup"><span data-stu-id="1ab19-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="1ab19-134">Como o local do projeto do Visual Studio padrão está no diretório do usuário atual e, portanto, não concede permissões de leitura ao grupo de usuários, você deve mover o. dll ou alterar as ACLs para permitir acesso SearchFilterHost.exe.</span><span class="sxs-lookup"><span data-stu-id="1ab19-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="1ab19-135">Ao registrar um novo manipulador de filtro, recomendamos que você use um nome descritivo, por exemplo, o IFilter HTML.</span><span class="sxs-lookup"><span data-stu-id="1ab19-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="1ab19-136">**Para registrar seu novo manipulador de filtro:**</span><span class="sxs-lookup"><span data-stu-id="1ab19-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="1ab19-137">Especifique a extensão e o GUID do manipulador persistente que usarão o manipulador de filtro:</span><span class="sxs-lookup"><span data-stu-id="1ab19-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="1ab19-138">Registre seu manipulador de filtro com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="1ab19-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="1ab19-139">Abordagem obsoleta para registrar manipuladores de filtros</span><span class="sxs-lookup"><span data-stu-id="1ab19-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="1ab19-140">Essa abordagem não é recomendada para uso.</span><span class="sxs-lookup"><span data-stu-id="1ab19-140">This approach is not recommended for use.</span></span> <span data-ttu-id="1ab19-141">Os filtros podem ser registrados para um CLSID que representa uma classe COM (Component Object Model) e/ou para uma extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ab19-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="1ab19-142">Você poderia registrar ambos os filtros se precisar registrar um manipulador de filtro para uma classe e um manipulador de filtro diferente para uma extensão de nome de arquivo dentro da classe.</span><span class="sxs-lookup"><span data-stu-id="1ab19-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="1ab19-143">Observe que um manipulador de filtro registrado para uma extensão de nome de arquivo tem precedência sobre um manipulador de filtro para um CLSID.</span><span class="sxs-lookup"><span data-stu-id="1ab19-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="1ab19-144">Essas entradas são entradas de registro OLE padrão até e incluindo a entrada para o CLSID de classe **\\ {ApplicationGUID}**.</span><span class="sxs-lookup"><span data-stu-id="1ab19-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="1ab19-145">A DLL sample.dll implementa o comportamento de objeto em execução para a classe. txt.</span><span class="sxs-lookup"><span data-stu-id="1ab19-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="1ab19-146">Observe a entrada extra, PersistentHandler.</span><span class="sxs-lookup"><span data-stu-id="1ab19-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="1ab19-147">Essa entrada especifica a classe responsável pelas solicitações de agente para os objetos persistentes da classe de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1ab19-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="1ab19-148">A entrada em **PersistentAddinsRegistered** identifica a implementação responsável pela interface chamada **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter).</span><span class="sxs-lookup"><span data-stu-id="1ab19-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="1ab19-149">A classe implementando o **\_ IFilter de IID** tem entradas de registro OLE padrão.</span><span class="sxs-lookup"><span data-stu-id="1ab19-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="1ab19-150">A DLL InprocServer32 é carregada por meio do mecanismo OLE padrão.</span><span class="sxs-lookup"><span data-stu-id="1ab19-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="1ab19-151">O Windows Search observa o modelo de threading especificado para o manipulador de filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab19-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="1ab19-152">Quando o modelo de threading é definido como **ambos**, o manipulador de filtro deve ser thread-safe; caso contrário, se não for thread-safe, especifique **Apartment**.</span><span class="sxs-lookup"><span data-stu-id="1ab19-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="1ab19-153">Observe que os manipuladores de filtro sempre devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ab19-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="1ab19-154">As entradas de registro de exemplo a seguir são para um manipulador de filtro registrado para uma extensão de nome de arquivo e classe.</span><span class="sxs-lookup"><span data-stu-id="1ab19-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="1ab19-155">**{PersistentHandlerGUID}** e **{FilterHandlerCLSID}** são usados como variáveis indicando valores que precisam ser especificados pelo criador do manipulador de filtro.</span><span class="sxs-lookup"><span data-stu-id="1ab19-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="1ab19-156">Os valores são do tipo REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="1ab19-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="1ab19-157">Substituindo manipuladores de filtro existentes</span><span class="sxs-lookup"><span data-stu-id="1ab19-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="1ab19-158">Recomendamos que você não substitua os manipuladores de filtro internos para tipos de arquivo comuns, como. txt,. doc,. html,. URL e assim por diante, pois isso pode ter efeitos indesejados em outros componentes do sistema.</span><span class="sxs-lookup"><span data-stu-id="1ab19-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="1ab19-159">A indexação de corpos de mensagens de email depende dos manipuladores de filtro. txt,. html e. rtf, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="1ab19-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="1ab19-160">Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtro for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="1ab19-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="1ab19-161">Não há nenhum mecanismo para encadear filtros.</span><span class="sxs-lookup"><span data-stu-id="1ab19-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="1ab19-162">Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.</span><span class="sxs-lookup"><span data-stu-id="1ab19-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="1ab19-163">Localizando um manipulador de filtro para uma determinada extensão de arquivo</span><span class="sxs-lookup"><span data-stu-id="1ab19-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="1ab19-164">Você pode usar a interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para localizar um manipulador de filtro para uma determinada extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ab19-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="1ab19-165">As entradas de registro de exemplo a seguir ilustram como fazer isso para arquivos HTML.</span><span class="sxs-lookup"><span data-stu-id="1ab19-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="1ab19-166">Neste exemplo, o manipulador de filtro para documentos HTML é nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="1ab19-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="1ab19-167">Os valores são do tipo REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="1ab19-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="1ab19-168">**Para localizar o manipulador de filtro para uma determinada extensão de nome de arquivo:**</span><span class="sxs-lookup"><span data-stu-id="1ab19-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="1ab19-169">Verifique se a extensão do tipo de arquivos filtrado tem um manipulador persistente registrado na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Extension.</span><span class="sxs-lookup"><span data-stu-id="1ab19-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="1ab19-170">Nesse caso, deixe que essa chave seja {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="1ab19-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="1ab19-171">Se não houver um manipulador persistente registrado para a extensão, localize o CLSID associado ao tipo de documento na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="1ab19-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="1ab19-172">Permita que essa chave seja {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="1ab19-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="1ab19-173">Em seguida, determine se um manipulador persistente está registrado para o CLSID: usando {ApplicationGUID} localize o manipulador persistente para a \\ entrada de classe de software do hKey \_ local \_ Machine \\ \\ classes \\ CLSID \\ {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="1ab19-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="1ab19-174">Permita que essa chave seja {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="1ab19-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="1ab19-175">Determine o GUID do manipulador persistente: usando {PersistentHandlerGUID} localize o GUID do manipulador persistente para o tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="1ab19-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="1ab19-176">O valor na entrada do registro HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF produz o GUID do manipulador persistente para esse tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="1ab19-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="1ab19-177">Permita que essa chave seja {FilterHandlerCLSID}.</span><span class="sxs-lookup"><span data-stu-id="1ab19-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="1ab19-178">Determine o manipulador de filtro: usando {FilterHandlerCLSID} que foi determinado na etapa anterior, localize o manipulador de filtro na entrada \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32.</span><span class="sxs-lookup"><span data-stu-id="1ab19-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="1ab19-179">Neste exemplo, o nome do manipulador de filtro descritivo usado é o IFilter HTML.</span><span class="sxs-lookup"><span data-stu-id="1ab19-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="1ab19-180">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1ab19-180">Additional Resources</span></span>

- <span data-ttu-id="1ab19-181">O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para implementar a interface **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="1ab19-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="1ab19-182">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1ab19-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="1ab19-183">Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1ab19-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="1ab19-184">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ab19-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ab19-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ab19-185">Related topics</span></span>

[<span data-ttu-id="1ab19-186">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="1ab19-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="1ab19-187">Sobre manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="1ab19-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="1ab19-188">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="1ab19-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="1ab19-189">Retornando Propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="1ab19-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="1ab19-190">Manipuladores de filtro que acompanham o Windows</span><span class="sxs-lookup"><span data-stu-id="1ab19-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="1ab19-191">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="1ab19-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="1ab19-192">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="1ab19-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
