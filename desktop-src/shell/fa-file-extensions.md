---
description: O registro de um tipo de arquivo é a primeira etapa na criação de uma associação de arquivo, que torna esse tipo de arquivo &\# 0034; conhecido&\# 0034; para o Shell. No entanto, sem manipuladores de tipo de arquivo, o shell não consegue expor informações ao usuário do e sobre o arquivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Manipuladores de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827013"
---
# <a name="file-type-handlers"></a><span data-ttu-id="c394e-104">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-104">File Type Handlers</span></span>

<span data-ttu-id="c394e-105">O [registro de um tipo de arquivo](fa-how-work.md) é a primeira etapa na criação de uma associação de arquivo, que torna esse tipo de arquivo "conhecido" para o Shell.</span><span class="sxs-lookup"><span data-stu-id="c394e-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="c394e-106">No entanto, sem manipuladores de tipo de arquivo, o shell não consegue expor informações ao usuário do e sobre o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c394e-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="c394e-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c394e-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c394e-108">Criar um tipo de arquivo conhecido pelo shell</span><span class="sxs-lookup"><span data-stu-id="c394e-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="c394e-109">Descrições do manipulador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="c394e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c394e-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="c394e-111">Criar um tipo de arquivo conhecido pelo shell</span><span class="sxs-lookup"><span data-stu-id="c394e-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="c394e-112">Na captura de tela a seguir do Windows Explorer, o arquivo de imagem deserto. conhecido aparece na biblioteca **imagens** do Shell e está associado somente ao aplicativo Paint.</span><span class="sxs-lookup"><span data-stu-id="c394e-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![captura de tela mostrando o Explorer abrindo uma imagem sem nenhum tipo de arquivo](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="c394e-114">O arquivo deserto. known na captura de tela anterior não tem a seguinte funcionalidade habilitada por um manipulador de tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="c394e-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="c394e-115">Miniatura ou visualização</span><span class="sxs-lookup"><span data-stu-id="c394e-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="c394e-116">Verbos específicos de imagem no menu de atalho, como:</span><span class="sxs-lookup"><span data-stu-id="c394e-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="c394e-117">Girar visualização</span><span class="sxs-lookup"><span data-stu-id="c394e-117">Rotate Preview</span></span>
    -   <span data-ttu-id="c394e-118">Definir como plano de fundo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="c394e-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="c394e-119">Imprimir</span><span class="sxs-lookup"><span data-stu-id="c394e-119">Print</span></span>
-   <span data-ttu-id="c394e-120">Propriedades específicas da imagem no painel de **detalhes** , como:</span><span class="sxs-lookup"><span data-stu-id="c394e-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="c394e-121">Data de início</span><span class="sxs-lookup"><span data-stu-id="c394e-121">Date Taken</span></span>
    -   <span data-ttu-id="c394e-122">Marcações</span><span class="sxs-lookup"><span data-stu-id="c394e-122">Tags</span></span>
    -   <span data-ttu-id="c394e-123">Classificação</span><span class="sxs-lookup"><span data-stu-id="c394e-123">Rating</span></span>
-   <span data-ttu-id="c394e-124">Indexação do texto do arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-124">Indexing of file text</span></span>

<span data-ttu-id="c394e-125">Na captura de tela a seguir, o mesmo arquivo (deserto. known) tem a extensão. jpg, que é um tipo de arquivo registrado que tem manipuladores de tipo de arquivo associados, portanto, uma imagem em miniatura e mais propriedades são mostradas.</span><span class="sxs-lookup"><span data-stu-id="c394e-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![imagem com um tipo de arquivo registrado e manipuladores de tipo de arquivo associados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="c394e-127">Descrições do manipulador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="c394e-128">A funcionalidade fornecida por cada manipulador de tipo de arquivo está listada na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="c394e-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="c394e-129">Manipulador</span><span class="sxs-lookup"><span data-stu-id="c394e-129">Handler</span></span>                                                      | <span data-ttu-id="c394e-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c394e-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c394e-131">Menu de atalho</span><span class="sxs-lookup"><span data-stu-id="c394e-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="c394e-132">Um manipulador de menu de atalho, às vezes chamado de manipulador de menu de contexto, é um manipulador de tipo de arquivo que adiciona comandos a um menu de contexto existente.</span><span class="sxs-lookup"><span data-stu-id="c394e-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="c394e-133">Esses manipuladores estão associados a um determinado tipo de arquivo e são chamados sempre que um menu de contexto é exibido para um membro do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c394e-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c394e-134">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="c394e-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="c394e-135">Um manipulador que fornece uma imagem para representar um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="c394e-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="c394e-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c394e-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="c394e-137">Um manipulador de propriedades que fornece acesso às propriedades do item para o Windows Search, o Windows Explorer e outros aplicativos que precisam acessar propriedades.</span><span class="sxs-lookup"><span data-stu-id="c394e-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c394e-138">Visualização</span><span class="sxs-lookup"><span data-stu-id="c394e-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="c394e-139">Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item a ser exibido no painel de visualização do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="c394e-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c394e-140">Filtros</span><span class="sxs-lookup"><span data-stu-id="c394e-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="c394e-141">Um filtro, uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , que examina os documentos em busca de texto e Propriedades (também chamados de atributos).</span><span class="sxs-lookup"><span data-stu-id="c394e-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="c394e-142">Ele extrai partes do texto desses documentos, filtrando a formatação inserida e mantendo as informações sobre a posição do texto.</span><span class="sxs-lookup"><span data-stu-id="c394e-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="c394e-143">Ele também extrai partes de valores, que são propriedades de um documento inteiro ou de partes bem definidas de um documento.</span><span class="sxs-lookup"><span data-stu-id="c394e-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="c394e-144">O **IFilter** fornece a base para a criação de aplicativos de nível superior, como indexadores de documentos e visualizadores independentes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c394e-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c394e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c394e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c394e-146">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c394e-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="c394e-147">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="c394e-148">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="c394e-149">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="c394e-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="c394e-150">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c394e-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="c394e-151">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="c394e-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="c394e-152">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="c394e-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="c394e-153">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="c394e-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
