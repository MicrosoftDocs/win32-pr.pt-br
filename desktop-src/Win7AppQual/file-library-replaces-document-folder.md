---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: A biblioteca de arquivos substitui a pasta de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836950"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="c41c3-103">A biblioteca de arquivos substitui a pasta de documentos</span><span class="sxs-lookup"><span data-stu-id="c41c3-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c41c3-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="c41c3-104">Affected Platforms</span></span>

<span data-ttu-id="c41c3-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="c41c3-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="c41c3-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c41c3-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="c41c3-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="c41c3-107">Feature Impact</span></span>

<span data-ttu-id="c41c3-108">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="c41c3-108">**Severity** - Medium</span></span>  
<span data-ttu-id="c41c3-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="c41c3-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="c41c3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c41c3-110">Description</span></span>

<span data-ttu-id="c41c3-111">As bibliotecas fornecem uma experiência de pasta centralizada para armazenamento de arquivos, pesquisa e acesso em vários locais, tanto locais quanto remotos.</span><span class="sxs-lookup"><span data-stu-id="c41c3-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="c41c3-112">Os locais padrão usados por caixas de diálogo de arquivo comuns (por exemplo, abrir e salvar) foram alterados da pasta de documentos para a biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="c41c3-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="c41c3-113">A interface do usuário está inalterada, mas o usuário agora poderá exibir, procurar e pesquisar a biblioteca usando várias exibições de organização.</span><span class="sxs-lookup"><span data-stu-id="c41c3-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="c41c3-114">Os arquivos serão salvos no local de salvamento padrão da biblioteca, a menos que o usuário altere o local de salvamento padrão ou escolha uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="c41c3-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="c41c3-115">Os desenvolvedores podiam criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes usando a interface IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="c41c3-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="c41c3-116">Os usuários podem encontrar bibliotecas usando o sistema de pastas conhecido (por exemplo, FOLDERid \_ DocumentsLibrary).</span><span class="sxs-lookup"><span data-stu-id="c41c3-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="c41c3-117">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="c41c3-117">Manifestation of Impact</span></span>

<span data-ttu-id="c41c3-118">A biblioteca é, em si, um arquivo, e não uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c41c3-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="c41c3-119">Portanto, as manipulações de caminho podem resultar em erros devido à tentativa pelo aplicativo de concatenar arquivos em arquivos.</span><span class="sxs-lookup"><span data-stu-id="c41c3-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="c41c3-120">Solução</span><span class="sxs-lookup"><span data-stu-id="c41c3-120">Solution</span></span>

<span data-ttu-id="c41c3-121">Ao usar IFileDialog, você deve usar o método GetResult em vez de combinação de GetFolder e GetFilename como faria nas versões anteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c41c3-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="c41c3-122">Use as APIs do shell sempre que possível para interagir com e manipular itens no namespace do Shell (por exemplo, IShellItem).</span><span class="sxs-lookup"><span data-stu-id="c41c3-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="c41c3-123">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="c41c3-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="c41c3-124">Se você quiser criar suas próprias bibliotecas ou adicionar locais a bibliotecas existentes, deverá usar a API IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="c41c3-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="c41c3-125">As bibliotecas são pastas de shell próprias para que você possa enumerá-las assim como qualquer outra pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="c41c3-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="c41c3-126">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="c41c3-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="c41c3-127">Usar a caixa de diálogo arquivo comum garantirá que os usuários possam salvar diretamente em suas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="c41c3-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c41c3-128">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="c41c3-128">Links to Other Resources</span></span>

-   <span data-ttu-id="c41c3-129">**Bibliotecas do Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="c41c3-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="c41c3-130">**Mantendo a sincronização com uma biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="c41c3-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



