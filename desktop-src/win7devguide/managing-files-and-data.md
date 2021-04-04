---
title: Gerenciando arquivos e dados
description: Os usuários têm acesso mais fácil a arquivos e dados no Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917458"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="a8e73-103">Gerenciando arquivos e dados</span><span class="sxs-lookup"><span data-stu-id="a8e73-103">Managing Files and Data</span></span>

<span data-ttu-id="a8e73-104">Os usuários têm acesso mais fácil a arquivos e dados no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8e73-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="a8e73-105">Novas APIs tornam os arquivos e exibições mais informativos, permitindo que os aplicativos forneçam informações relevantes e diferenciadas ao Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="a8e73-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="a8e73-106">Além disso, os aplicativos se beneficiam do novo modelo de *bibliotecas* , uma noção mais abstrata e útil do espaço de armazenamento do usuário que as pastas e também podem participar de bibliotecas comuns de tipos de arquivos semelhantes que são compartilhados por diferentes aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a8e73-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="a8e73-107">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="a8e73-107">Libraries</span></span>

<span data-ttu-id="a8e73-108">O Windows 7 apresenta o conceito de *bibliotecas* como destinos em que os desenvolvedores e os usuários finais podem localizar e organizar seus dados como coleções de itens que podem abranger vários locais no computador local, bem como em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="a8e73-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="a8e73-109">As APIs de *biblioteca* fornecem uma maneira simples para os desenvolvedores criarem aplicativos que criam, interagem com e dão suporte a *bibliotecas* como itens de primeira classe em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a8e73-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="a8e73-110">As *bibliotecas* também podem ser selecionadas usando a caixa de diálogo Seletor de pasta.</span><span class="sxs-lookup"><span data-stu-id="a8e73-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="a8e73-111">Os aplicativos podem enumerar escopos de biblioteca relevantes ou podem usar a biblioteca diretamente como uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a8e73-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="a8e73-112">(Consulte bibliotecas do [Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) e [bibliotecas do Windows 7: recursos para desenvolvedores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span><span class="sxs-lookup"><span data-stu-id="a8e73-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![biblioteca de imagens do Windows 7](images/windows7-10.jpg)

<span data-ttu-id="a8e73-114">*Biblioteca de imagens* mostra suas imagens, independentemente de onde elas estão armazenadas</span><span class="sxs-lookup"><span data-stu-id="a8e73-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="a8e73-115">Formatos de arquivo e armazenamentos de dados</span><span class="sxs-lookup"><span data-stu-id="a8e73-115">File Formats and Data Stores</span></span>

<span data-ttu-id="a8e73-116">No Windows 7, o Windows Explorer facilita o gerenciamento e a manipulação de arquivos para o usuário de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="a8e73-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="a8e73-117">A visualização do tipo de arquivo de seu aplicativo é mais acessível com um novo botão que permite aos usuários mostrar e ocultar o painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="a8e73-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="a8e73-118">As pilhas visuais de imersão agregam imagens em miniatura para tipos de arquivo em uma exibição.</span><span class="sxs-lookup"><span data-stu-id="a8e73-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="a8e73-119">Os modos de exibição do Windows Explorer mostram informações úteis com base nas propriedades gravadas com seu manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8e73-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="a8e73-120">Trechos de documento e realce de visita usam a implementação da interface do **IFilter** para facilitar a pesquisa e a localização de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a8e73-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="a8e73-121">Os verbos e comandos do menu de contexto são mais fáceis do que nunca implementar.</span><span class="sxs-lookup"><span data-stu-id="a8e73-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="a8e73-122">Ao implementar todos os manipuladores de formato apropriados para os itens retornados do seu manipulador de protocolo, os resultados da pesquisa de seu armazenamento de dados personalizado podem ser tão ricos quanto os resultados da pesquisa de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a8e73-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="a8e73-123">As *bibliotecas* são criadas automaticamente para seus manipuladores de protocolo para que os usuários possam criar o escopo de suas pesquisas com facilidade.</span><span class="sxs-lookup"><span data-stu-id="a8e73-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="a8e73-124">E a lógica para a criação de *bibliotecas* pode ser facilmente personalizada por meio do registro.</span><span class="sxs-lookup"><span data-stu-id="a8e73-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="a8e73-125">(Consulte [desenvolvendo filtros para o Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="a8e73-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![biblioteca de documentos do Windows 7](images/windows7-11.jpg)

<span data-ttu-id="a8e73-127">No Windows 7, o Windows Explorer facilita o gerenciamento e a manipulação de arquivos</span><span class="sxs-lookup"><span data-stu-id="a8e73-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 