---
title: Documentos compostos
description: Os documentos OLE compostos permitem que os usuários trabalhem em um único aplicativo para manipular dados gravados em vários formatos e derivados de várias fontes.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084947"
---
# <a name="compound-documents"></a><span data-ttu-id="4c8f2-103">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="4c8f2-103">Compound Documents</span></span>

<span data-ttu-id="4c8f2-104">Os documentos OLE compostos permitem que os usuários trabalhem em um único aplicativo para manipular dados gravados em vários formatos e derivados de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="4c8f2-105">Por exemplo, um usuário pode inserir em um documento de processamento de texto um grafo criado em um segundo aplicativo e um objeto de som criado em um terceiro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="4c8f2-106">Ativar o grafo faz com que o segundo aplicativo carregue sua interface do usuário ou pelo menos essa parte que contém as ferramentas necessárias para editar o objeto.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="4c8f2-107">Ativar o objeto de som faz com que o terceiro aplicativo o execute.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="4c8f2-108">Em ambos os casos, um usuário é capaz de manipular dados de fontes externas de dentro do contexto de um único documento.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="4c8f2-109">A tecnologia de documento OLE composto está posicionada em uma base que consiste em COM, armazenamento estruturado e transferência de dados uniforme.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="4c8f2-110">Conforme resumido abaixo, cada uma dessas tecnologias principais desempenha uma função crítica em documentos compostos OLE:</span><span class="sxs-lookup"><span data-stu-id="4c8f2-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="4c8f2-111"><span id="COM"></span><span id="com"></span>INTERFACES</span><span class="sxs-lookup"><span data-stu-id="4c8f2-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="4c8f2-112">Um objeto de documento composto é essencialmente um objeto COM que pode ser inserido ou vinculado a um documento existente.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="4c8f2-113">Como um objeto COM, um objeto de documento composto expõe a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , por meio da qual os clientes podem obter ponteiros para suas outras interfaces, incluindo vários, como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), que fornecem recursos especiais exclusivos para objetos de documento compostos.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="4c8f2-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="4c8f2-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="4c8f2-115">Um objeto de documento composto deve implementar o [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) ou, opcionalmente, as interfaces [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para gerenciar seu próprio armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="4c8f2-116">Um contêiner usado para criar documentos compostos deve fornecer a interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , por meio da qual os objetos armazenam e recuperam dados.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="4c8f2-117">Os contêineres quase sempre fornecem instâncias de **IStorage** obtidas da implementação dos arquivos compostos do OLE.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="4c8f2-118">Os contêineres também devem usar as interfaces **IPersistStorage** e/ou **IPersistStream** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="4c8f2-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferência de Dados uniforme</span><span class="sxs-lookup"><span data-stu-id="4c8f2-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="4c8f2-120">Os aplicativos que dão suporte a documentos compostos devem implementar [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) porque objetos incorporados e vinculados começam como dados que foram transferidos usando formatos de área de transferência OLE especiais, em vez de formatos de área de transferência padrão do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="4c8f2-121">Em outras palavras, a formatação de dados como um objeto incorporado ou vinculado é simplesmente uma opção mais fornecida pelo modelo de transferência uniforme de dados do OLE.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="4c8f2-122">A tecnologia de documentos compostos do OLE beneficia os desenvolvedores de software e os usuários.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="4c8f2-123">Em vez de se sentir obrigada a CRAM cada recurso concebível em um único aplicativo, os desenvolvedores de software agora são gratuitos, se quiserem, para desenvolver aplicativos menores e mais focados que dependem de outros aplicativos para fornecer recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="4c8f2-124">Nos casos em que um desenvolvedor de software decide fornecer um aplicativo com recursos além de seus principais recursos, o desenvolvedor pode implementar esses serviços adicionais como DLLs separadas, que são carregadas na memória somente quando seus serviços são necessários.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="4c8f2-125">Os usuários se beneficiam de softwares menores, mais rápidos e mais compatíveis que podem misturar e corresponder conforme necessário, manipulando todos os componentes necessários de dentro de um único documento mestre.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="4c8f2-126">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="4c8f2-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4c8f2-127">Contêineres e servidores</span><span class="sxs-lookup"><span data-stu-id="4c8f2-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="4c8f2-128">Vinculação e inserção</span><span class="sxs-lookup"><span data-stu-id="4c8f2-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="4c8f2-129">Manipuladores de objetos</span><span class="sxs-lookup"><span data-stu-id="4c8f2-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="4c8f2-130">Servidores em processo</span><span class="sxs-lookup"><span data-stu-id="4c8f2-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="4c8f2-131">Objetos vinculados e monikers</span><span class="sxs-lookup"><span data-stu-id="4c8f2-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="4c8f2-132">Notificações</span><span class="sxs-lookup"><span data-stu-id="4c8f2-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="4c8f2-133">Interfaces de documento composto</span><span class="sxs-lookup"><span data-stu-id="4c8f2-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="4c8f2-134">Estados de objeto</span><span class="sxs-lookup"><span data-stu-id="4c8f2-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="4c8f2-135">Implementando a ativação do In-Place</span><span class="sxs-lookup"><span data-stu-id="4c8f2-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="4c8f2-136">Criando objetos vinculados e incorporados de dados existentes</span><span class="sxs-lookup"><span data-stu-id="4c8f2-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="4c8f2-137">Exibir cache</span><span class="sxs-lookup"><span data-stu-id="4c8f2-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="4c8f2-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c8f2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c8f2-139">Transferência de Dados</span><span class="sxs-lookup"><span data-stu-id="4c8f2-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="4c8f2-140">Armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="4c8f2-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 