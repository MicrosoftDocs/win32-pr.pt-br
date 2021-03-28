---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
title: Glossário do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296728"
---
# <a name="shell-glossary"></a><span data-ttu-id="6fd77-103">Glossário do Shell</span><span class="sxs-lookup"><span data-stu-id="6fd77-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="6fd77-104">Um</span><span class="sxs-lookup"><span data-stu-id="6fd77-104">A</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-105">**associação**</span><span class="sxs-lookup"><span data-stu-id="6fd77-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-106">Um mapeamento de uma extensão de nome de arquivo (por exemplo,. mp3) ou protocolo (por exemplo, http) para um identificador programático (ProgID).</span><span class="sxs-lookup"><span data-stu-id="6fd77-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="6fd77-107">Esse mapeamento é armazenado no registro como uma configuração por usuário com um fallback por computador.</span><span class="sxs-lookup"><span data-stu-id="6fd77-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="6fd77-108">Os aplicativos que participam do sistema de programas padrão definem o mapeamento de associação para a extensão de nome de arquivo ou protocolo para apontarem para as chaves ProgID que eles possuem.</span><span class="sxs-lookup"><span data-stu-id="6fd77-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-109">**matriz de associação**</span><span class="sxs-lookup"><span data-stu-id="6fd77-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-110">Uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="6fd77-111">Por exemplo, um arquivo. jpg tem a seguinte matriz de associação em um sistema Windows padrão: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "a \\ \\ imagem de SystemFileAssociations de HKCR", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".</span><span class="sxs-lookup"><span data-stu-id="6fd77-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="6fd77-112">B</span><span class="sxs-lookup"><span data-stu-id="6fd77-112">B</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="6fd77-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-114">Para carregar ou associar código a dados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-114">To load or associate code with data.</span></span> <span data-ttu-id="6fd77-115">Por exemplo, um manipulador pode ser associado a uma fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="6fd77-116">C</span><span class="sxs-lookup"><span data-stu-id="6fd77-116">C</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-117">**nome canônico**</span><span class="sxs-lookup"><span data-stu-id="6fd77-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-118">O nome exclusivo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6fd77-118">The unique name of a resource.</span></span> <span data-ttu-id="6fd77-119">Canônico significa "de acordo com as regras".</span><span class="sxs-lookup"><span data-stu-id="6fd77-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="6fd77-120">Consulte também: nome do verbo canônico.</span><span class="sxs-lookup"><span data-stu-id="6fd77-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-121">**nome do verbo canônico**</span><span class="sxs-lookup"><span data-stu-id="6fd77-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-122">Um nome com neutralidade de idioma que pode ser usado programaticamente para se referir a um verbo, independentemente da cadeia de caracteres localizada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6fd77-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="6fd77-123">Consulte também: nome canônico, verbo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-124">**contêiner**</span><span class="sxs-lookup"><span data-stu-id="6fd77-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-125">Um tipo de item de shell que pode conter outros itens.</span><span class="sxs-lookup"><span data-stu-id="6fd77-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="6fd77-126">Os itens em um contêiner são expostos ao namespace do shell usando uma fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="6fd77-127">Os exemplos incluem pastas, unidades, servidores de rede e arquivos compactados com uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="6fd77-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="6fd77-128">Consulte também: fonte de dados do Shell, pasta, item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-129">**content**</span><span class="sxs-lookup"><span data-stu-id="6fd77-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-130">Texto e propriedades associados a um item de shell ou a uma fonte de conteúdo que pode ser indexada.</span><span class="sxs-lookup"><span data-stu-id="6fd77-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-131">**fonte de conteúdo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-132">Um item que pode ser acessado pelo indexador.</span><span class="sxs-lookup"><span data-stu-id="6fd77-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="6fd77-133">As fontes de conteúdo são endereçáveis por uma URL e são fornecidas ao indexador por um manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="6fd77-134">Os exemplos incluem: arquivos e pastas do sistema de arquivos, itens e pastas do Microsoft Outlook, registros de banco de dados e itens armazenados do Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6fd77-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="6fd77-135">Uma fonte de conteúdo pode ser exposta como itens de shell implementando uma fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="6fd77-136">Consulte também: conteúdo, item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-137">**content view (exibição de conteúdo)**</span><span class="sxs-lookup"><span data-stu-id="6fd77-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-138">Uma exibição no Windows Explorer (oferecida no Windows 7 e posterior) que exibe o conteúdo mais relevante para cada item da lista com base em sua associação de tipo ou extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="6fd77-139">A exibição de conteúdo usa uma lógica de redimensionamento que descarta Propriedades quando o tamanho da janela diminui para garantir que as propriedades mais críticas ainda tenham espaço para serem legíveis.</span><span class="sxs-lookup"><span data-stu-id="6fd77-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="6fd77-140">Consulte também: padrão de layout, tipo, associação de tipo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-141">**modo de exibição de conteúdo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-142">Confira definição para: exibição de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-143">**menu de contexto**</span><span class="sxs-lookup"><span data-stu-id="6fd77-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-144">Esse termo às vezes é usado para significar o menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="6fd77-145">Consulte definição para: menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-146">**manipulador de menu de contexto**</span><span class="sxs-lookup"><span data-stu-id="6fd77-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-147">Esse termo às vezes é usado para significar o manipulador de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="6fd77-148">Consulte a definição de: manipulador de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="6fd77-149">D</span><span class="sxs-lookup"><span data-stu-id="6fd77-149">D</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-150">**manipulador de objeto de dados**</span><span class="sxs-lookup"><span data-stu-id="6fd77-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-151">Um manipulador que fornece formatos de área de transferência adicionais para o objeto de dados (IDataObject) de um item.</span><span class="sxs-lookup"><span data-stu-id="6fd77-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="6fd77-152">Os objetos de dados são usados nos cenários de arrastar e soltar e copiar/colar.</span><span class="sxs-lookup"><span data-stu-id="6fd77-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-153">**fonte de dados**</span><span class="sxs-lookup"><span data-stu-id="6fd77-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-154">Esse termo às vezes é usado para significar o armazenamento de dados ou a fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="6fd77-155">Consulte definição para: armazenamento de dados, fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-156">**armazenamento de dados**</span><span class="sxs-lookup"><span data-stu-id="6fd77-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-157">Um repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-157">A repository of data.</span></span> <span data-ttu-id="6fd77-158">Um armazenamento de dados pode ser exposto ao modelo de programação do shell como um contêiner usando uma fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="6fd77-159">Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-160">**composição de área de trabalho**</span><span class="sxs-lookup"><span data-stu-id="6fd77-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-161">Um recurso do Windows Vista que permite que janelas individuais sejam desenhadas para superfícies fora da tela na memória de vídeo em vez de serem desenhadas diretamente para o dispositivo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="6fd77-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-162">**document**</span><span class="sxs-lookup"><span data-stu-id="6fd77-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-163">Um item de shell que contém texto e para o qual a interface IFilter poderia ser implementada.</span><span class="sxs-lookup"><span data-stu-id="6fd77-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-164">**descartar manipulador**</span><span class="sxs-lookup"><span data-stu-id="6fd77-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-165">Um manipulador que permite que um determinado tipo de item dê suporte a cenários de arrastar e soltar e copiar/colar.</span><span class="sxs-lookup"><span data-stu-id="6fd77-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-166">**soltar destino**</span><span class="sxs-lookup"><span data-stu-id="6fd77-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-167">Um objeto de dados que é arrastado e descartado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="6fd77-168">Consulte também: manipulador de dados, descartar manipulador.</span><span class="sxs-lookup"><span data-stu-id="6fd77-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-169">**verbo dinâmico**</span><span class="sxs-lookup"><span data-stu-id="6fd77-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-170">Um verbo que depende do estado de um item de shell ou do sistema; a aparência do item é baseada em estado e requer que o código de execução determine se o item deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="6fd77-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="6fd77-171">Consulte também: manipulador de menu de atalho, verbo estático, verbo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="6fd77-172">E</span><span class="sxs-lookup"><span data-stu-id="6fd77-172">E</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-173">**Comando do Explorer**</span><span class="sxs-lookup"><span data-stu-id="6fd77-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-174">Um objeto que pode ser apresentado como um botão próximo à parte superior da janela do Windows Explorer que fornece funcionalidade para itens e contêineres nessa janela.</span><span class="sxs-lookup"><span data-stu-id="6fd77-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="6fd77-175">Uma fonte de dados do Shell fornece os objetos de comando do Windows Explorer para um item de contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="6fd77-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="6fd77-176">Os comandos às vezes são usados como verbos.</span><span class="sxs-lookup"><span data-stu-id="6fd77-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="6fd77-177">F</span><span class="sxs-lookup"><span data-stu-id="6fd77-177">F</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-178">**Associação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-179">Consulte a definição para: Associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-180">**formato de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-181">Um formato para dados armazenados em um arquivo que tem uma especificação de formato documentado.</span><span class="sxs-lookup"><span data-stu-id="6fd77-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="6fd77-182">Os exemplos incluem o OLE DOCFILE, OPC, XML, ZIP e outras especificações de formato de arquivo conhecidas.</span><span class="sxs-lookup"><span data-stu-id="6fd77-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="6fd77-183">Os criadores de tipo de arquivo geralmente usam um formato de arquivo existente como a base de um novo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="6fd77-184">Um formato de arquivo pode ser simplesmente uma definição que não é instanciada como um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-185">**manipulador de formato de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-186">Este termo é um sinônimo para o manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="6fd77-187">Consulte a definição para: manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-188">**extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-189">O indicador principal de um tipo de arquivo para itens do sistema de arquivos, é a parte do nome do arquivo que segue o ponto final.</span><span class="sxs-lookup"><span data-stu-id="6fd77-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="6fd77-190">A extensão de nome de arquivo não pode conter espaços ou caracteres não ASCII e aplica-se somente a arquivos (não pastas).</span><span class="sxs-lookup"><span data-stu-id="6fd77-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="6fd77-191">As extensões de nome de arquivo são comparadas usando uma função de comparação que não é sensível ao caso ou à localidade.</span><span class="sxs-lookup"><span data-stu-id="6fd77-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="6fd77-192">Consulte também: formato de arquivo, tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-193">**tipo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-194">Um valor de extensão de nome de arquivo específico, como ". htm" ou ". jpg", que define uma classe de arquivos que são do mesmo tipo e têm um conjunto comum de associações.</span><span class="sxs-lookup"><span data-stu-id="6fd77-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="6fd77-195">Consulte também: tipo, associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-196">**associação de tipo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-197">Para uma extensão de nome de arquivo específica, os elementos da matriz de associação que definem onde os manipuladores e outros atributos podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="6fd77-198">Consulte também: matriz de associação, tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-199">**personalização de tipo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-200">Uma associação que habilita o Shell a personalizar como o Shell trata um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="6fd77-201">As personalizações de tipo de arquivo incluem: especificar o aplicativo usado para abrir o arquivo quando clicado duas vezes, adicionando comandos ao menu de atalho para um tipo de arquivo, especificando um ícone personalizado, especificando um tipo de conteúdo MIME para associar a um tipo de arquivo, especificando um tipo percebido e especificando um ou mais aplicativos associados por tipo de arquivo com a caixa de diálogo abrir com.</span><span class="sxs-lookup"><span data-stu-id="6fd77-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="6fd77-202">Consulte também: Percebidotype.</span><span class="sxs-lookup"><span data-stu-id="6fd77-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-203">**manipulador de tipo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-204">Um manipulador registrado para um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-204">A handler registered for a file type.</span></span> <span data-ttu-id="6fd77-205">Consulte também: manipulador.</span><span class="sxs-lookup"><span data-stu-id="6fd77-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-206">**pasta**</span><span class="sxs-lookup"><span data-stu-id="6fd77-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-207">Consulte a definição para: contêiner.</span><span class="sxs-lookup"><span data-stu-id="6fd77-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-208">**PIDL completo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-209">Um PIDL que descreve exclusivamente um objeto relativo à pasta da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="6fd77-210">H</span><span class="sxs-lookup"><span data-stu-id="6fd77-210">H</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-211">**cliques**</span><span class="sxs-lookup"><span data-stu-id="6fd77-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-212">Um objeto COM que fornece funcionalidade para um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="6fd77-213">A maioria das fontes de dados de shell oferece um sistema extensível para ligar manipuladores a itens.</span><span class="sxs-lookup"><span data-stu-id="6fd77-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="6fd77-214">Por exemplo, a pasta sistema de arquivos usa o sistema de associação para pesquisar os manipuladores de um determinado tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="6fd77-215">Consulte também: Associação de arquivo, tipo de arquivo, personalização de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="6fd77-216">I</span><span class="sxs-lookup"><span data-stu-id="6fd77-216">I</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-217">**manipulador de ícone**</span><span class="sxs-lookup"><span data-stu-id="6fd77-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-218">Um manipulador que fornece as informações necessárias para gerar e armazenar em cache um ícone para um item.</span><span class="sxs-lookup"><span data-stu-id="6fd77-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="6fd77-219">O armazenamento de dados do sistema de arquivos dá suporte ao carregamento de um manipulador de ícones para um item com base no tipo de arquivo, permitindo que esse manipulador forneça um ícone que é usado para todas as instâncias desse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-220">**manipulador InfoTip**</span><span class="sxs-lookup"><span data-stu-id="6fd77-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-221">Um manipulador que fornece texto pop-up quando o usuário passa o ponteiro do mouse sobre um objeto da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6fd77-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-222">**item**</span><span class="sxs-lookup"><span data-stu-id="6fd77-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-223">Consulte a definição de: item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-224">**classe de item**</span><span class="sxs-lookup"><span data-stu-id="6fd77-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-225">Consulte definição para: tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-226">**lista de identificadores de item**</span><span class="sxs-lookup"><span data-stu-id="6fd77-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-227">Sequência de uma ou mais estruturas SHITEMID que define exclusivamente um objeto em relação a algum objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="6fd77-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="6fd77-228">K</span><span class="sxs-lookup"><span data-stu-id="6fd77-228">K</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-229">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-230">Uma propriedade que fornece um nome de tipo amigável e pode ser associada a uma lista de propriedades e um padrão de layout.</span><span class="sxs-lookup"><span data-stu-id="6fd77-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="6fd77-231">O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo para o usuário final e foi definido como uma propriedade de cadeia de caracteres com vários valores (valores de cadeia de caracteres canônicos), assim, você pode ter um valor de tipo de "áudio; vídeo" ou "vincular; documento".</span><span class="sxs-lookup"><span data-stu-id="6fd77-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="6fd77-232">Alguns nomes de tipos amigáveis do usuário já estão associados a propriedades e padrões de layout.</span><span class="sxs-lookup"><span data-stu-id="6fd77-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="6fd77-233">Por exemplo, itens associados ao tipo. imagem e itens associados a Kind.Document exibem propriedades diferentes mesmo quando estão na mesma exibição.</span><span class="sxs-lookup"><span data-stu-id="6fd77-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="6fd77-234">Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout.</span><span class="sxs-lookup"><span data-stu-id="6fd77-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="6fd77-235">Consulte também: espécie de associação, exibição de conteúdo, padrão de layout.</span><span class="sxs-lookup"><span data-stu-id="6fd77-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="6fd77-236">L</span><span class="sxs-lookup"><span data-stu-id="6fd77-236">L</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-237">**padrão de layout**</span><span class="sxs-lookup"><span data-stu-id="6fd77-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-238">Uma das várias disposições para exibir propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fd77-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="6fd77-239">No Windows 7 e posterior, ao registrar um novo tipo de arquivo, você pode usar a exibição de conteúdo para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="6fd77-240">Você pode escolher entre quatro padrões de layout diferentes: alfa (para resultados de pesquisa de documentos que contêm trechos de código), beta (para resultados de pesquisa de email com trechos de código), gama (semelhante a alfa, mas com um layout de duas linhas em vez de quatro) e Delta (para mostrar muitas propriedades mais curtas, como com música e imagens).</span><span class="sxs-lookup"><span data-stu-id="6fd77-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="6fd77-241">Consulte também: exibição de conteúdo, tipo, associação de tipo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="6fd77-242">M</span><span class="sxs-lookup"><span data-stu-id="6fd77-242">M</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-243">**manipulador de metadados**</span><span class="sxs-lookup"><span data-stu-id="6fd77-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-244">Esse termo às vezes é usado para significar o manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fd77-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="6fd77-245">Consulte a definição de: manipulador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6fd77-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="6fd77-246">N</span><span class="sxs-lookup"><span data-stu-id="6fd77-246">N</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-247">**extensão do namespace**</span><span class="sxs-lookup"><span data-stu-id="6fd77-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-248">Consulte a definição de: fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="6fd77-249">O</span><span class="sxs-lookup"><span data-stu-id="6fd77-249">O</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-250">**Banco de dados de vinculação e incorporação de objetos (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="6fd77-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-251">Um conjunto padrão de interfaces que fornece acesso heterogêneo a fontes diferentes de informações localizadas em qualquer lugar, como sistemas de arquivos, pastas de email e bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="6fd77-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-253">Consulte definição para: vinculação de objetos e banco de dados de incorporação.</span><span class="sxs-lookup"><span data-stu-id="6fd77-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="6fd77-254">P</span><span class="sxs-lookup"><span data-stu-id="6fd77-254">P</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="6fd77-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-256">Uma categoria ampla de tipos de formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-256">A broad category of file format types.</span></span> <span data-ttu-id="6fd77-257">O percebidatype foi introduzido no Windows XP e dá suporte a um conjunto limitado de tipos de arquivo conhecidos (exemplos incluem imagem, texto, áudio e tipos de arquivo compactados).</span><span class="sxs-lookup"><span data-stu-id="6fd77-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="6fd77-258">Tipos de arquivo, geralmente tipos de arquivo públicos, também podem ter um tipo percebido.</span><span class="sxs-lookup"><span data-stu-id="6fd77-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="6fd77-259">Por exemplo, o arquivo de imagem Types. bmp,. png,. jpg e. gif também são do tipo percebido, Image.</span><span class="sxs-lookup"><span data-stu-id="6fd77-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="6fd77-260">Na camada de programação, Percebidotype é expresso como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="6fd77-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="6fd77-261">Como há código que usa tipo e Percebidotype, os proprietários de formato de arquivo devem registrar ambos.</span><span class="sxs-lookup"><span data-stu-id="6fd77-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="6fd77-262">Por exemplo, "reproduzir tudo" depende de Percebidotype.</span><span class="sxs-lookup"><span data-stu-id="6fd77-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="6fd77-263">Consulte também: tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-264">**Gerenciador de visualização**</span><span class="sxs-lookup"><span data-stu-id="6fd77-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-265">Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item de Shell a ser exibido no painel de visualização do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6fd77-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-266">**manipulador de propriedades**</span><span class="sxs-lookup"><span data-stu-id="6fd77-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-267">Um manipulador que traduz dados armazenados em um arquivo em um esquema estruturado que é reconhecido pelo e pode ser acessado pelo Windows Explorer, pelo Windows Search e por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fd77-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="6fd77-268">Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="6fd77-269">Os dados traduzidos incluem exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6fd77-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="6fd77-270">Cada manipulador de propriedade é associado a um tipo de arquivo específico, identificado pela extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="6fd77-271">Consulte também: sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fd77-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-272">**manipulador de folhas de propriedades**</span><span class="sxs-lookup"><span data-stu-id="6fd77-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-273">Um manipulador que é usado para criar folhas de propriedades personalizadas com imagens e controles da interface do usuário que permitem a interação personalizada com um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-274">**sistema de propriedades**</span><span class="sxs-lookup"><span data-stu-id="6fd77-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-275">Um sistema de leitura/gravação extensível de definições de dados que usa propriedades implementadas como pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="6fd77-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="6fd77-276">Consulte também: manipulador de propriedades, item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-277">**valor da propriedade**</span><span class="sxs-lookup"><span data-stu-id="6fd77-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-278">Um valor associado a um nome de propriedade para um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="6fd77-279">Por exemplo, "autor", "tamanho" e "data de uso" são propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fd77-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="6fd77-280">Os valores de propriedade são expressos como uma estrutura PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="6fd77-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-281">**manipulador de protocolo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-282">Um manipulador que acessa fontes de conteúdo e fornece um objeto IUrlAccessor para um protocolo e uma URL especificados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="6fd77-283">Os manipuladores de protocolo estendem a funcionalidade de pesquisa do Windows e podem fornecer notificações de alteração aos indexadores.</span><span class="sxs-lookup"><span data-stu-id="6fd77-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="6fd77-284">Manipuladores de protocolo diferentes são necessários para indexar tipos específicos de armazenamentos de dados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="6fd77-285">Para fornecer uma experiência de usuário razoável, você também deve fornecer uma fonte de dados do Shell para o armazenamento de dados, além de implementar seu manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="6fd77-286">O manipulador de protocolo expõe os itens no armazenamento de dados para o indexador, enquanto a fonte de dados do Shell expõe os itens no armazenamento de dados para o Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="6fd77-287">R</span><span class="sxs-lookup"><span data-stu-id="6fd77-287">R</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-288">**PIDL relativo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-289">Um PIDL que é relativo a algum objeto raiz no namespace do shell que não seja a pasta da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="6fd77-290">Normalmente, essa é a pasta pai do item.</span><span class="sxs-lookup"><span data-stu-id="6fd77-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="6fd77-291">S</span><span class="sxs-lookup"><span data-stu-id="6fd77-291">S</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-292">**Fonte de dados do Shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-293">Um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="6fd77-294">No passado, a fonte de dados do Shell era chamada de extensão de namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="6fd77-295">Consulte também: contêiner, manipulador, item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-296">**Extensão do shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-297">Esse termo às vezes é usado para significar o manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6fd77-298">Consulte a definição para: manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-299">**Manipulador de extensão de Shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-300">Esse termo às vezes é usado para significar o manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6fd77-301">Consulte a definição para: manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-302">**Manipulador de Shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-303">Esse termo às vezes é usado para significar o manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="6fd77-304">Consulte a definição para: manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-305">**Item do Shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-306">Uma única parte do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-306">A single piece of content.</span></span> <span data-ttu-id="6fd77-307">Alguns itens de shell são fontes de conteúdo e outros não.</span><span class="sxs-lookup"><span data-stu-id="6fd77-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="6fd77-308">Uma pasta é uma fonte de conteúdo, por exemplo, mas um arquivo. jpg não é.</span><span class="sxs-lookup"><span data-stu-id="6fd77-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="6fd77-309">Manipuladores de tipo de arquivo expõem itens de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="6fd77-310">Em alguns contextos, "item" é usado para distinguir contêineres de não contidos.</span><span class="sxs-lookup"><span data-stu-id="6fd77-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="6fd77-311">Consulte também: contêiner, fonte de conteúdo, manipulador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd77-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-312">**Extensão do namespace do Shell**</span><span class="sxs-lookup"><span data-stu-id="6fd77-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-313">Esse termo às vezes é usado para significar a fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="6fd77-314">Consulte a definição de: fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-315">**menu de atalho**</span><span class="sxs-lookup"><span data-stu-id="6fd77-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-316">Uma interface do usuário que é usada para apresentar uma coleção de verbos associados a um elemento de interface do usuário, como um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6fd77-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-317">**Manipulador de menu de atalho**</span><span class="sxs-lookup"><span data-stu-id="6fd77-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-318">Um manipulador que adiciona verbos para um item ou itens.</span><span class="sxs-lookup"><span data-stu-id="6fd77-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="6fd77-319">Esses verbos são normalmente exibidos em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="6fd77-320">Consulte também: menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-321">**PIDL simples**</span><span class="sxs-lookup"><span data-stu-id="6fd77-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-322">Um PIDL que é analisado sem verificação de disco.</span><span class="sxs-lookup"><span data-stu-id="6fd77-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-323">**verbo estático**</span><span class="sxs-lookup"><span data-stu-id="6fd77-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-324">Um verbo que se aplica a um item de shell sem a necessidade de inspecionar o estado atual de um item ou sistema.</span><span class="sxs-lookup"><span data-stu-id="6fd77-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="6fd77-325">Um verbo estático é baseado em um registro estático dos elementos associados de um item e não é alterado.</span><span class="sxs-lookup"><span data-stu-id="6fd77-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="6fd77-326">T</span><span class="sxs-lookup"><span data-stu-id="6fd77-326">T</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-327">**manipulador de miniaturas**</span><span class="sxs-lookup"><span data-stu-id="6fd77-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-328">Um manipulador que fornece uma imagem estática para representar um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-329">**provedor de miniatura**</span><span class="sxs-lookup"><span data-stu-id="6fd77-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-330">Esse termo às vezes é usado para significar o manipulador de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="6fd77-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="6fd77-331">Consulte a definição de: manipulador de miniatura.</span><span class="sxs-lookup"><span data-stu-id="6fd77-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="6fd77-332">U</span><span class="sxs-lookup"><span data-stu-id="6fd77-332">U</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-333">**nome de tipo amigável do usuário**</span><span class="sxs-lookup"><span data-stu-id="6fd77-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-334">Consulte a definição de: Kind.</span><span class="sxs-lookup"><span data-stu-id="6fd77-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="6fd77-335">V</span><span class="sxs-lookup"><span data-stu-id="6fd77-335">V</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-336">**verbo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-337">Uma ação individual que pode ser chamada por um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="6fd77-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="6fd77-338">Os exemplos incluem abrir e imprimir.</span><span class="sxs-lookup"><span data-stu-id="6fd77-338">Examples include open and print.</span></span> <span data-ttu-id="6fd77-339">Os verbos são, às vezes, chamados de comandos ou tarefas.</span><span class="sxs-lookup"><span data-stu-id="6fd77-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="6fd77-340">Consulte também: verbo dinâmico, manipulador de menu de atalho, verbo estático.</span><span class="sxs-lookup"><span data-stu-id="6fd77-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-341">**manipulador de verbo**</span><span class="sxs-lookup"><span data-stu-id="6fd77-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-342">Esse termo às vezes é usado para significar o manipulador de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="6fd77-343">Consulte a definição de: manipulador de menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6fd77-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



