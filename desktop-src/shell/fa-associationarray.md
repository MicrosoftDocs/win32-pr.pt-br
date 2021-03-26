---
description: Uma matriz de associação é uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo.
title: Matrizes de associação
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090240"
---
# <a name="association-arrays"></a><span data-ttu-id="7f6bc-103">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="7f6bc-103">Association Arrays</span></span>

<span data-ttu-id="7f6bc-104">Uma matriz de associação é uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="7f6bc-105">O Shell usa matrizes de associação para consultar um conjunto predefinido de locais de registro que podem conter informações sobre um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="7f6bc-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7f6bc-107">Sobre matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="7f6bc-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="7f6bc-108">Consultando matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="7f6bc-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="7f6bc-109">Trabalhando com matrizes de associação para uma determinada fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="7f6bc-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="7f6bc-110">Matrizes de associação de fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="7f6bc-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="7f6bc-111">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7f6bc-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7f6bc-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f6bc-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="7f6bc-113">Sobre matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="7f6bc-113">About Association Arrays</span></span>

<span data-ttu-id="7f6bc-114">Uma matriz de associação é uma lista ordenada de locais de registro que contêm informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="7f6bc-115">Essas informações sobre o tipo de item podem ser registradas em diferentes níveis de especificidade.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="7f6bc-116">Por exemplo, você pode registrar um verbo que será exibido apenas para um tipo de arquivo específico (como. jpg) ou para todos os itens com o mesmo System. Kind (por exemplo, System. Kind = Picture) ou para todos os itens.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="7f6bc-117">O Shell usa matrizes de associação para consultar um conjunto predefinido de locais de registro que podem potencialmente conter informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="7f6bc-118">As APIs da matriz de associação podem ser usadas para recuperar da subchave do registro um único valor que contém as informações solicitadas, com esse valor proveniente da primeira entrada na matriz que a fornece.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="7f6bc-119">Por exemplo, o valor de ícone padrão é recuperado dessa forma.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="7f6bc-120">A matriz de associação também pode ser usada para recuperar um conjunto de valores que são armazenados nas subchaves do registro.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="7f6bc-121">Por exemplo, a lista de verbos é criada a partir dos verbos que são registrados em todas as subchaves.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="7f6bc-122">Depois que o Shell consulta um conjunto predefinido de locais de registro para obter informações sobre um item de Shell, ele coloca os locais do registro em uma matriz na ordem do local mais específico para o mais geral.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="7f6bc-123">Como as matrizes de associação são listas ordenadas, elas fornecem aos desenvolvedores de aplicativos um mecanismo para adicionar informações ao registro que serão retornadas para um tipo específico de item.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="7f6bc-124">Da mesma forma, as matrizes de associação permitem que os desenvolvedores de aplicativos adicionem informações ao registro para um grupo específico de itens quando esses itens são registrados em um local mais geral.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="7f6bc-125">Essa lógica informa sua decisão sobre o local mais apropriado no registro para armazenar informações sobre itens de Shell.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="7f6bc-126">Em um sistema Windows padrão, um arquivo. jpg tem a seguinte matriz de associação:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="7f6bc-127">**HKEY \_ Jpgfile de classes \_ raiz** \\ </span><span class="sxs-lookup"><span data-stu-id="7f6bc-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="7f6bc-128">**HKEY \_ CLASSES \_ raiz** \\ **SystemFileAssociations** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="7f6bc-129">**HKEY \_ Imagem \_ raiz de classes** \\ </span><span class="sxs-lookup"><span data-stu-id="7f6bc-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="7f6bc-130">**HKEY \_ CLASSES \_ raiz** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="7f6bc-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="7f6bc-131">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="7f6bc-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="7f6bc-132">Para obter informações sobre como registrar matrizes de associação, consulte [registro de aplicativo](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="7f6bc-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="7f6bc-133">Consultando matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="7f6bc-133">Querying Association Arrays</span></span>

<span data-ttu-id="7f6bc-134">Há APIs do Shell para recuperar informações de uma variedade de subchaves do registro, da subchave do registro mais específica para um superconjunto das informações em todas as subchaves do registro.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="7f6bc-135">O uso mais comum de uma matriz de associação é consultar um único valor que o Shell retorna do elemento mais específico na matriz que tem as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="7f6bc-136">O exemplo de código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="7f6bc-137">As APIs a seguir podem ser usadas para consultar uma matriz de associação ou para construir um objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de matriz de associação que pode ser consultado:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="7f6bc-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (antes do Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="7f6bc-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="7f6bc-139">**AssocCreateForClasses**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="7f6bc-140">**AssocQueryString**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="7f6bc-141">Trabalhando com matrizes de associação para uma determinada fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="7f6bc-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="7f6bc-142">Cada fonte de dados do Shell define a matriz de associação para seus itens.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="7f6bc-143">A definição de uma matriz de associação geralmente é uma função do tipo de item.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="7f6bc-144">Os implementadores de fonte de dados do Shell devem definir e documentar as matrizes de associação para permitir que os aplicativos estendam o comportamento desses tipos, como para o registro de verbos ou outras informações.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="7f6bc-145">Os aplicativos podem estender o comportamento de itens com base na adição de dados às subchaves da matriz de associação, como a adição de verbos para itens.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="7f6bc-146">A fonte de dados do sistema de arquivos cria uma matriz de associação para arquivos com base nas seguintes subchaves de registro e ProgIDs especiais:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="7f6bc-147">Se o arquivo tiver um ProgID registrado, a ProgID de **\_ \_ raiz das classes hKey** \\  será usada.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="7f6bc-148">Caso contrário, a **\_ \_ raiz de classes hKey** \\ **desconhecida** será usada.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="7f6bc-149">A extensão de nome de arquivo é registrada na subchave **HKEY \_ classes \_ raiz** \\ **SystemFileAssociations** \\ *. FileExtension* .</span><span class="sxs-lookup"><span data-stu-id="7f6bc-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="7f6bc-150">ProgIDs especiais são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="7f6bc-151">ProgID especial</span><span class="sxs-lookup"><span data-stu-id="7f6bc-151">Special progID</span></span>                                    | <span data-ttu-id="7f6bc-152">Description</span><span class="sxs-lookup"><span data-stu-id="7f6bc-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="7f6bc-153">**HKEY \_ CLASSES \_ raiz** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="7f6bc-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="7f6bc-154">Todos os arquivos (não pastas)</span><span class="sxs-lookup"><span data-stu-id="7f6bc-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="7f6bc-155">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="7f6bc-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="7f6bc-156">Arquivos e pastas do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="7f6bc-156">Files and file system folders</span></span> |
    | <span data-ttu-id="7f6bc-157">**HKEY \_ Diretório \_ raiz de classes** \\ </span><span class="sxs-lookup"><span data-stu-id="7f6bc-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="7f6bc-158">Pastas do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="7f6bc-158">File system folders</span></span>           |
    | <span data-ttu-id="7f6bc-159">**HKEY \_ Pasta \_ raiz de classes** \\ </span><span class="sxs-lookup"><span data-stu-id="7f6bc-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="7f6bc-160">Contêineres do Shell</span><span class="sxs-lookup"><span data-stu-id="7f6bc-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="7f6bc-161">Matrizes de associação de fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="7f6bc-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="7f6bc-162">A lista a seguir representa algumas das matrizes de associação de armazenamento de dados do shell que podem ser usadas para as finalidades descritas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="7f6bc-163">**HKEY \_ CLASSES \_ raiz** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="7f6bc-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="7f6bc-164">_ *HKEY \_ classes \_ root **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="7f6bc-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="7f6bc-165">**HKEY \_ \_Raiz de classes** \\ **Kind.Document**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="7f6bc-166">**HKEY \_ Resultados \_ raiz de classes** \\ </span><span class="sxs-lookup"><span data-stu-id="7f6bc-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="7f6bc-167">**HKEY \_ CLASSES \_ raiz** \\ **SystemFileAssociations** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="7f6bc-168">**HKEY \_ \_Raiz de classes** \\ **Word.Document. 12**</span><span class="sxs-lookup"><span data-stu-id="7f6bc-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="7f6bc-169">As matrizes de associação de fonte de dados do shell que podem ser usadas para DBFolder (um armazenamento de dados do shell que representa itens nos resultados da pesquisa e exibições baseadas em consulta) são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="7f6bc-170">Unidades</span><span class="sxs-lookup"><span data-stu-id="7f6bc-170">Drives</span></span>
-   <span data-ttu-id="7f6bc-171">Rede</span><span class="sxs-lookup"><span data-stu-id="7f6bc-171">Network</span></span>
-   <span data-ttu-id="7f6bc-172">RegItems</span><span class="sxs-lookup"><span data-stu-id="7f6bc-172">RegItems</span></span>
-   <span data-ttu-id="7f6bc-173">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="7f6bc-173">Examples:</span></span>
    -   <span data-ttu-id="7f6bc-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="7f6bc-174">ContentView</span></span>
    -   <span data-ttu-id="7f6bc-175">Verbos</span><span class="sxs-lookup"><span data-stu-id="7f6bc-175">Verbs</span></span>

<span data-ttu-id="7f6bc-176">Outras matrizes de associação comuns incluem pastas e impressoras.</span><span class="sxs-lookup"><span data-stu-id="7f6bc-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f6bc-177">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7f6bc-177">Additional Resources</span></span>

-   <span data-ttu-id="7f6bc-178">Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="7f6bc-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f6bc-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f6bc-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6bc-180">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-181">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-182">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-183">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-184">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-185">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="7f6bc-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-186">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="7f6bc-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="7f6bc-187">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="7f6bc-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
