---
description: O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do registro. Por meio do registro, tanto os implementadores quanto os terceiros podem permitir que os manipuladores de protocolo novos e herdados participem da pesquisa do Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Criando um conector de pesquisa para um manipulador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090095"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="5fdb4-104">Criando um conector de pesquisa para um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="5fdb4-105">O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="5fdb4-106">Por meio do registro, tanto os implementadores quanto os terceiros podem permitir que os manipuladores de protocolo novos e herdados participem da pesquisa do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="5fdb4-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5fdb4-108">Sobre os conectores de pesquisa para manipuladores de protocolo no Windows 7</span><span class="sxs-lookup"><span data-stu-id="5fdb4-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="5fdb4-109">Habilitando manipuladores de protocolo para participar da pesquisa</span><span class="sxs-lookup"><span data-stu-id="5fdb4-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="5fdb4-110">Desabilitando a criação do conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="5fdb4-111">Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="5fdb4-112">Usando o redirecionamento de cadeia de caracteres do registro</span><span class="sxs-lookup"><span data-stu-id="5fdb4-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="5fdb4-113">Restaurando um conector de pesquisa de manipulador de protocolo excluído</span><span class="sxs-lookup"><span data-stu-id="5fdb4-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="5fdb4-114">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5fdb4-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5fdb4-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fdb4-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="5fdb4-116">Sobre os conectores de pesquisa para manipuladores de protocolo no Windows 7</span><span class="sxs-lookup"><span data-stu-id="5fdb4-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="5fdb4-117">No Windows 7, as pesquisas no menu **Iniciar** ou no Windows Explorer incluem apenas arquivos em locais indexados e itens que não são do sistema de arquivos, como armazenamentos de dados remotos ou itens de manipulador de protocolo que têm um conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="5fdb4-118">Além de incluir os itens de manipulador de protocolo no escopo do menu **Iniciar** e das pesquisas do Shell, o conector de pesquisa habilita o menu **Iniciar** para agrupar itens de manipulador de protocolo nos resultados do menu **Iniciar** , com o benefício resultante de que o usuário pode clicar no cabeçalho do grupo e exibir os resultados somente do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="5fdb4-119">Como alternativa, o usuário pode navegar até a pasta **pesquisas** , abrir o arquivo do conector de pesquisa e executar uma pesquisa que inclui apenas itens do manipulador de protocolo específico associado a esse conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="5fdb4-120">Quando um usuário inicia pela primeira vez um aplicativo que registra um manipulador de protocolo, o Windows Explorer gera um arquivo do conector de pesquisa (. searchConnector-MS) para o manipulador de protocolo na pasta **pesquisas** do usuário.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="5fdb4-121">Os aplicativos com manipuladores de protocolo podem optar por desabilitar esse comportamento ou personalizar o nome e a descrição do conector de pesquisa do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="5fdb4-122">O local da pasta de **pesquisas** do usuário é% USERPROFILE% de \\ pesquisas ou FolderId \_ SavedSearches.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="5fdb4-123">O GUID para FOLDERid \_ SavedSearches é {7d1d3a04-Debb-4115-95cf-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="5fdb4-124">O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do Registro descritas nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="5fdb4-125">Habilitando manipuladores de protocolo para participar da pesquisa</span><span class="sxs-lookup"><span data-stu-id="5fdb4-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="5fdb4-126">Desabilitando a criação do conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="5fdb4-127">Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="5fdb4-128">Restaurando um conector de pesquisa de manipulador de protocolo excluído</span><span class="sxs-lookup"><span data-stu-id="5fdb4-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="5fdb4-129">Não há meios programáticos para criar um conector de pesquisa para um manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="5fdb4-130">Eles devem ser configurados por meio do registro.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="5fdb4-131">Habilitando manipuladores de protocolo para participar da pesquisa</span><span class="sxs-lookup"><span data-stu-id="5fdb4-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="5fdb4-132">As chaves do registro e seus valores possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="5fdb4-133">Um manipulador de protocolo pode popular algumas ou todas essas chaves do registro <protocol> , onde é substituído pelo nome real de seu protocolo, como MAPI, arquivo ou CSC, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="5fdb4-134">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="5fdb4-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="5fdb4-135">Valor (es) possível (is)</span><span class="sxs-lookup"><span data-stu-id="5fdb4-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="5fdb4-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-136">Type</span></span>       | <span data-ttu-id="5fdb4-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fdb4-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdb4-138">HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ versão</span><span class="sxs-lookup"><span data-stu-id="5fdb4-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="5fdb4-139">Não existe (padrão).</span><span class="sxs-lookup"><span data-stu-id="5fdb4-139">Does not exist (default).</span></span> <span data-ttu-id="5fdb4-140">Caso contrário, será 1 ou maior.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="5fdb4-141">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5fdb4-141">REG\_DWORD</span></span> | <span data-ttu-id="5fdb4-142">Esse valor é usado para detectar alterações nos registros de modelo de localização para raízes de pesquisa que já foram processadas.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="5fdb4-143">Se não existir, use 0 como padrão.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="5fdb4-144">Como alternativa, aumente a versão para informar ao Windows Explorer que o conector de pesquisa deve ser regenerado porque uma versão mais recente do manipulador de protocolo foi instalada.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="5fdb4-145">HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors</span><span class="sxs-lookup"><span data-stu-id="5fdb4-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="5fdb4-146">Não existe (padrão).</span><span class="sxs-lookup"><span data-stu-id="5fdb4-146">Does not exist (default).</span></span> <span data-ttu-id="5fdb4-147">Caso contrário, defina como 1.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="5fdb4-148">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5fdb4-148">REG\_DWORD</span></span> | <span data-ttu-id="5fdb4-149">Se não existir, crie um arquivo. searchconnector-MS na pasta pesquisas.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="5fdb4-150">Se 1, marque como processado e não faça nada.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="5fdb4-151">HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ Descrição padrão</span><span class="sxs-lookup"><span data-stu-id="5fdb4-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="5fdb4-152">Uma cadeia de caracteres localizável que contém a descrição do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="5fdb4-153">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="5fdb4-153">REG\_SZ</span></span>    | <span data-ttu-id="5fdb4-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-154">Optional.</span></span> <span data-ttu-id="5fdb4-155">Ele é usado no elemento Description do arquivo. searchconnector-MS.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5fdb4-156">HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ nome padrão</span><span class="sxs-lookup"><span data-stu-id="5fdb4-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="5fdb4-157">Uma cadeia de caracteres localizada para nomear o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-157">A localized string to name the search connector.</span></span> <span data-ttu-id="5fdb4-158">Usado como o nome do arquivo. searchconnector-MS.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="5fdb4-159">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="5fdb4-159">REG\_SZ</span></span>    | <span data-ttu-id="5fdb4-160">Cada local deve ter um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-160">Each location must have a unique name.</span></span> <span data-ttu-id="5fdb4-161">Na ausência desse valor, o nome de exibição fornecido pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do manipulador de protocolo será usado.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="5fdb4-162">HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ padrão \\ FolderType</span><span class="sxs-lookup"><span data-stu-id="5fdb4-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="5fdb4-163">Um GUID que identifica o [FOLDERTYPEID](../shell/foldertypeid.md) a ser aplicado ao conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="5fdb4-164">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="5fdb4-164">REG\_SZ</span></span>    | <span data-ttu-id="5fdb4-165">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-165">Optional.</span></span> <span data-ttu-id="5fdb4-166">Usado no elemento FolderType do arquivo. searchconnector-MS para indicar quais modelos devem ser usados para exibir os resultados.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="5fdb4-167">Por exemplo, o valor de GUID de \_ documentos FOLDERTYPEID.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="5fdb4-168">Desabilitando a criação do conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="5fdb4-169">Se seu aplicativo expõe itens por meio de um manipulador de protocolo para uso no próprio aplicativo e você não deseja expor os itens por meio do Shell (no menu **Iniciar** e pesquisas do Windows Explorer), você precisa desabilitar a criação de um conector de pesquisa para o manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="5fdb4-170">Para desabilitar a criação do conector de pesquisa, defina DoNotCreateSearchConnectors como 0x00000001 (1), conforme mostrado no exemplo de chave do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="5fdb4-171">Se DoNotCreateSearchConnectors for definido como 1, recomendamos que você exponha a propriedade [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) em cada item exposto pelo manipulador de protocolo e defina o valor dessa propriedade como **true**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="5fdb4-172">Isso impedirá que os itens do manipulador de protocolo apareçam no grupo de **arquivos** do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5fdb4-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="5fdb4-173">Se DoNotCreateSearchConnectors estiver presente e definido como zero, o Windows Explorer criará um conector de pesquisa para o manipulador de protocolo e os itens do manipulador de protocolo serão retornados no menu **Iniciar** e nas pesquisas do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="5fdb4-174">Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="5fdb4-175">O nome do conector de pesquisa é usado não apenas para identificar o conector de pesquisa na pasta **pesquisas** , mas como o cabeçalho do grupo para os resultados em pesquisas do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5fdb4-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="5fdb4-176">Portanto, é importante fornecer um nome descritivo para o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="5fdb4-177">Se um nome não for fornecido na chave do registro, por padrão, o Windows Explorer usará o nome fornecido pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para a raiz de pesquisa do manipulador de protocolo e a descrição em branco.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="5fdb4-178">Você pode substituir o nome padrão por meio de uma entrada de chave do registro sem precisar renomear a interface IShellFolder.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="5fdb4-179">Embora não seja tão visível quanto o nome do conector de pesquisa, você também pode substituir a descrição do conector de pesquisa, fornecendo sua própria descrição.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="5fdb4-180">Para substituir o nome ou a descrição padrão, defina as entradas conforme mostrado no exemplo de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="5fdb4-181">Além disso, a entrada FolderType pode ser definida como um dos GUIDs [FOLDERTYPEID](../shell/foldertypeid.md) .</span><span class="sxs-lookup"><span data-stu-id="5fdb4-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="5fdb4-182">O valor deve ser o GUID real e não seu nome.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="5fdb4-183">Por exemplo, {94d6ddcc-4a68-4175-A374-bd584a510b78} em vez de FOLDERTYPEID \_ Music.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="5fdb4-184">O GUID de um FOLDERTYPEID pode ser obtido no arquivo de cabeçalho Shlguid. h na [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5fdb4-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="5fdb4-185">Usando o redirecionamento de cadeia de caracteres do registro</span><span class="sxs-lookup"><span data-stu-id="5fdb4-185">Using Registry String Redirection</span></span>

<span data-ttu-id="5fdb4-186">Você pode usar uma [cadeia de caracteres redirecionada](../intl/using-registry-string-redirection.md) para garantir que o nome fornecido para o conector de pesquisa possa ser localizado.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="5fdb4-187">Você pode incluir cadeias de caracteres localizáveis para as chaves de registro Name e Description em vez de inserir a cadeia de caracteres real no registro.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="5fdb4-188">Para incluir uma cadeia de caracteres localizável para os valores de nome ou descrição, defina o valor conforme mostrado no exemplo de chave do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="5fdb4-189">A cadeia de caracteres localizável usa o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="5fdb4-190">@dllname.dll,-ResourceId, em que:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="5fdb4-191">@dllname.dll é o caminho para a DLL que contém o recurso de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5fdb4-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="5fdb4-192">ResourceId é a ID de recurso de inteiro do recurso de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5fdb4-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="5fdb4-193">O formato de uma cadeia de caracteres indireta, e uma cadeia de caracteres indireta anexada a um modificador de versão, é descrito na [função SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="5fdb4-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="5fdb4-194">Restaurando um conector de pesquisa de manipulador de protocolo excluído</span><span class="sxs-lookup"><span data-stu-id="5fdb4-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="5fdb4-195">Como os conectores de pesquisa são arquivos no computador do usuário, eles podem ser excluídos por engano.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="5fdb4-196">Para restaurar todos os conectores de pesquisa de manipulador de protocolo excluídos, restaure as bibliotecas padrão.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="5fdb4-197">Para tanto, abra o Windows Explorer, clique com o botão direito do mouse na pasta **bibliotecas** e selecione **restaurar bibliotecas padrão**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![captura de tela mostrando a opção de menu restaurar bibliotecas padrão](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="5fdb4-199">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5fdb4-199">Additional Resources</span></span>

-   [<span data-ttu-id="5fdb4-200">IShellItem:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="5fdb4-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="5fdb4-201">SIGDN \_ NORMALDISPLAY</span><span class="sxs-lookup"><span data-stu-id="5fdb4-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="5fdb4-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fdb4-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5fdb4-203">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5fdb4-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5fdb4-204">Noções básicas sobre manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-205">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-206">Notificando o índice das alterações</span><span class="sxs-lookup"><span data-stu-id="5fdb4-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-207">Adicionando ícones e menus de contexto</span><span class="sxs-lookup"><span data-stu-id="5fdb4-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-208">Exemplo de código: extensões de Shell para manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-209">Instalando e Registrando manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="5fdb4-210">Depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5fdb4-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
