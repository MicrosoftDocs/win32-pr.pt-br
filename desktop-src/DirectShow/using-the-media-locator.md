---
description: Usando o localizador de mídia
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Usando o localizador de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930091"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="9e7d6-103">Usando o localizador de mídia</span><span class="sxs-lookup"><span data-stu-id="9e7d6-103">Using the Media Locator</span></span>

<span data-ttu-id="9e7d6-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9e7d6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9e7d6-105">O localizador de mídia é um objeto auxiliar que verifica os nomes de arquivo e procura arquivos ausentes em diretórios locais ou de rede.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="9e7d6-106">O detector de mídia mantém um cache de caminhos de diretório onde encontrou com êxito os arquivos nas pesquisas anteriores.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="9e7d6-107">Para localizar um arquivo, ele pesquisa os diretórios em seu cache.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="9e7d6-108">Falhando, o detector de mídia pode exibir uma caixa de diálogo abrir arquivo para que o usuário localize um arquivo manualmente.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="9e7d6-109">Supondo que o usuário localize o arquivo, o localizador de mídia adiciona o novo diretório ao seu cache.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="9e7d6-110">O localizador de mídia expõe a interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="9e7d6-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="9e7d6-111">Normalmente, seu aplicativo não cria diretamente uma instância do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="9e7d6-112">Em vez disso, a linha do tempo e o mecanismo de processamento fornecem os métodos a seguir para validar nomes de arquivo usando o detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="9e7d6-113">Para validar os nomes de arquivo na linha do tempo, chame [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d6-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="9e7d6-114">Opcionalmente, esse método também atualiza os objetos de origem com os nomes de arquivo corretos.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="9e7d6-115">Para validar nomes de arquivo quando o projeto é renderizado, chame [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d6-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="9e7d6-116">Ambos os métodos usam sinalizadores que controlam o comportamento do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="9e7d6-117">Por exemplo, você pode restringir a pesquisa a diretórios locais.</span><span class="sxs-lookup"><span data-stu-id="9e7d6-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e7d6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e7d6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e7d6-119">Trabalhando com fontes</span><span class="sxs-lookup"><span data-stu-id="9e7d6-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



