---
description: Gravando um objeto de cabeçalho ASF para um novo arquivo
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Gravando um objeto de cabeçalho ASF para um novo arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773017"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="bb953-103">Gravando um objeto de cabeçalho ASF para um novo arquivo</span><span class="sxs-lookup"><span data-stu-id="bb953-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="bb953-104">O objeto ASF ContentInfo armazena informações do objeto de cabeçalho ASF para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bb953-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="bb953-105">Quando um arquivo ASF é criado ou modificado, o objeto de cabeçalho deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="bb953-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="bb953-106">Para fazer isso, o aplicativo deve fornecer o perfil de codificação do conteúdo ao objeto ContentInfo para que ele saiba as características do arquivo de mídia a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bb953-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="bb953-107">Para gravar um novo arquivo, você pode usar o objeto ContentInfo para:</span><span class="sxs-lookup"><span data-stu-id="bb953-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="bb953-108">Coletar informações de cabeçalho do objeto de perfil do arquivo a ser criado,</span><span class="sxs-lookup"><span data-stu-id="bb953-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="bb953-109">Preencher vários objetos de cabeçalho na biblioteca ASF mantidos internamente pelo Media Foundation,</span><span class="sxs-lookup"><span data-stu-id="bb953-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="bb953-110">Inicializar o [Multiplexador de ASF](asf-multiplexer.md) para geração de pacotes de dados ASF e</span><span class="sxs-lookup"><span data-stu-id="bb953-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="bb953-111">Construa o objeto de cabeçalho de nível superior no formato binário que pode ser gravado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bb953-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="bb953-112">Para obter informações sobre perfis, consulte [perfil ASF](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="bb953-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="bb953-113">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="bb953-113">This section contains the following topics:</span></span>



| <span data-ttu-id="bb953-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="bb953-114">Topic</span></span>                                                                                                              | <span data-ttu-id="bb953-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb953-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb953-116">Inicializando o objeto ContentInfo de um novo arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="bb953-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="bb953-117">Descreve o método [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) que inicializa o objeto ContentInfo com informações de cabeçalho armazenadas em um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="bb953-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="bb953-118">Definindo propriedades no objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="bb953-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="bb953-119">Informações sobre várias propriedades de configuração que devem ser definidas no objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="bb953-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="bb953-120">Gerando um novo objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="bb953-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="bb953-121">Como gerar um buffer de mídia, que contém o objeto de cabeçalho ASF real do novo arquivo, a partir do objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="bb953-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="bb953-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb953-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb953-123">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="bb953-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="bb953-124">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="bb953-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="bb953-125">Estrutura de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="bb953-125">ASF File Structure</span></span>
</dt> </dl>

 

 



