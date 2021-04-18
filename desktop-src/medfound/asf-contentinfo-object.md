---
description: Objeto ASF ContentInfo
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objeto ASF ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796064"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="7b43c-103">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="7b43c-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="7b43c-104">O objeto ASF *ContentInfo* armazena informações do objeto de cabeçalho ASF de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b43c-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="7b43c-105">Um aplicativo pode usar o objeto ContentInfo para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="7b43c-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="7b43c-106">Ler o objeto de cabeçalho para um arquivo de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="7b43c-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="7b43c-107">Nesse caso, o objeto ContentInfo analisa o objeto de cabeçalho e armazena informações sobre o arquivo de características.</span><span class="sxs-lookup"><span data-stu-id="7b43c-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="7b43c-108">Media Foundation expõe várias dessas propriedades por meio de atributos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="7b43c-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="7b43c-109">Elas são descritas em [atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b43c-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="7b43c-110">Gravar informações de cabeçalho e construir um objeto de cabeçalho para um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b43c-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="7b43c-111">Inicialize outros objetos ASF, como o [divisor ASF](asf-splitter.md), o [multiplexador ASF](asf-multiplexer.md)e o indexador ASF, ao ler ou gravar um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7b43c-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="7b43c-112">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7b43c-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="7b43c-113">Criando o objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="7b43c-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="7b43c-114">Para criar uma nova instância do objeto ContentInfo, chame a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="7b43c-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="7b43c-115">Esse método retorna um ponteiro para um objeto ContentInfo vazio que deve ser inicializado para funcionar com um arquivo ASF específico.</span><span class="sxs-lookup"><span data-stu-id="7b43c-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="7b43c-116">Dependendo se o aplicativo está lendo um arquivo existente ou gravando um novo arquivo ASF, ele deve chamar [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ou [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para preencher o objeto vazio.</span><span class="sxs-lookup"><span data-stu-id="7b43c-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="7b43c-117">Para obter mais informações sobre essas chamadas de método, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7b43c-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="7b43c-118">Lendo o objeto de cabeçalho ASF de um arquivo existente</span><span class="sxs-lookup"><span data-stu-id="7b43c-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="7b43c-119">Obtendo informações de objetos de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="7b43c-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="7b43c-120">Gravando um objeto de cabeçalho ASF para um novo arquivo</span><span class="sxs-lookup"><span data-stu-id="7b43c-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="7b43c-121">Atributos de Media Foundation para objetos de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="7b43c-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="7b43c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b43c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b43c-123">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="7b43c-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



