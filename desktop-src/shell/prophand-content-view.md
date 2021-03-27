---
description: Este tópico descreve uma nova exibição no Windows Explorer, chamada exibição de conteúdo, que exibe o conteúdo mais relevante para cada item.
title: Exibição de conteúdo por tipo de arquivo ou tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662442"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="e1e43-103">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="e1e43-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="e1e43-104">Este tópico descreve uma nova exibição no Windows Explorer, chamada exibição de conteúdo, que exibe o conteúdo mais relevante para cada item.</span><span class="sxs-lookup"><span data-stu-id="e1e43-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="e1e43-105">Usando um conjunto de chaves do registro, os itens podem definir uma lista de propriedades e um layout que o Shell usa para a exibição de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e1e43-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="e1e43-106">O Shell recupera as chaves do registro usando a matriz de [Associação](fa-perceivedtypes.md)do item.</span><span class="sxs-lookup"><span data-stu-id="e1e43-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="e1e43-107">Como funciona a exibição de conteúdo?</span><span class="sxs-lookup"><span data-stu-id="e1e43-107">How Does the Content View Work?</span></span>

<span data-ttu-id="e1e43-108">No Windows 7 e posterior, a exibição de conteúdo usa uma lógica de redimensionamento que descarta Propriedades quando o tamanho da janela diminui, para garantir que as propriedades mais críticas ainda tenham espaço para serem legíveis.</span><span class="sxs-lookup"><span data-stu-id="e1e43-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="e1e43-109">A captura de tela a seguir ilustra a exibição de conteúdo dos resultados da pesquisa que contêm música, imagens e documentos.</span><span class="sxs-lookup"><span data-stu-id="e1e43-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![exibição de conteúdo dos resultados da pesquisa que contêm música, imagens e documentos](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="e1e43-111">Algumas fontes de dados do Shell usam a exibição de conteúdo por padrão, mas os usuários podem selecionar o modo de exibição de conteúdo clicando no botão de **controle exibir** no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e1e43-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="e1e43-112">Uma fonte de dados do Shell estende o namespace do Shell e expõe os itens em um armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="e1e43-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="e1e43-113">Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e1e43-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="e1e43-114">Como implementar o modo de exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e1e43-114">How to Implement the Content View</span></span>

<span data-ttu-id="e1e43-115">Ao registrar um novo [tipo de arquivo](fa-file-types.md) ou [manipulador de protocolo](../search/-search-3x-wds-extidx-prot-implementing.md), você pode aproveitar o modo de exibição de conteúdo usando uma das duas abordagens diferentes.</span><span class="sxs-lookup"><span data-stu-id="e1e43-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="e1e43-116">Você pode usar um conjunto existente de propriedades e padrão de layout, ou pode criar sua própria combinação.</span><span class="sxs-lookup"><span data-stu-id="e1e43-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="e1e43-117">Você pode usar uma entrada de registro para associar o tipo de arquivo ou o item a um [tipo](../properties/building-property-handlers-user-friendly-kind-names.md)predefinido, que é uma propriedade que você pode considerar como uma categoria de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e1e43-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="e1e43-118">Ao associar o tipo de arquivo ou o item a alguns desses tipos, você herdará automaticamente os padrões de layout da exibição de conteúdo e as listas de propriedades do tipo.</span><span class="sxs-lookup"><span data-stu-id="e1e43-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="e1e43-119">O Windows define padrões de layout de exibição de conteúdo e listas de propriedades para os seguintes tipos: documentos, email, pasta, música, imagem e genérico.</span><span class="sxs-lookup"><span data-stu-id="e1e43-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="e1e43-120">Esse tipo de associação é incentivado.</span><span class="sxs-lookup"><span data-stu-id="e1e43-120">This type of association is encouraged.</span></span> <span data-ttu-id="e1e43-121">Ele permite que você forneça a experiência consistente que um usuário espera para itens semelhantes.</span><span class="sxs-lookup"><span data-stu-id="e1e43-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="e1e43-122">Para obter mais informações, consulte [tipos de arquivo](fa-file-types.md) e nomes de [tipo](../properties/building-property-handlers-user-friendly-kind-names.md) e [como registrar uma exibição de conteúdo exclusiva conjunto de propriedades e padrão de layout para o tipo de arquivo ou item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="e1e43-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1e43-123">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="e1e43-123">Additional Resources</span></span>

-   <span data-ttu-id="e1e43-124">Para obter a documentação de referência de propriedade, consulte [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="e1e43-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="e1e43-125">Para obter a documentação de referência da PropList, consulte [System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)e [System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="e1e43-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1e43-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1e43-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e43-127">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e1e43-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="e1e43-128">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="e1e43-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="e1e43-129">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="e1e43-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="e1e43-130">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="e1e43-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="e1e43-131">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="e1e43-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="e1e43-132">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="e1e43-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="e1e43-133">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="e1e43-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="e1e43-134">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="e1e43-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
