---
title: Fluxos arbitrários
description: Fluxos arbitrários
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- SDK do Windows Media Format, fluxos arbitrários
- ASF (Advanced Systems Format), fluxos arbitrários
- ASF (formato de sistemas avançados), fluxos arbitrários
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos arbitrários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635025"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="101e6-110">Fluxos arbitrários</span><span class="sxs-lookup"><span data-stu-id="101e6-110">Arbitrary Streams</span></span>

<span data-ttu-id="101e6-111">Além dos fluxos de áudio e vídeo e fluxos de imagem, um arquivo ASF pode acomodar fluxos contendo uma variedade de dados.</span><span class="sxs-lookup"><span data-stu-id="101e6-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="101e6-112">Os objetos do Windows Media Format SDK fornecem suporte para fluxos de script, fluxos de transferência de arquivos, fluxos da Web e fluxos de dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="101e6-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="101e6-113">Todos esses tipos de fluxo são arbitrários, o que significa que nenhuma validação de dados é executada pelo objeto de leitura.</span><span class="sxs-lookup"><span data-stu-id="101e6-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="101e6-114">Quando você inclui fluxos desses tipos em seus arquivos, certifique-se de que o aplicativo de leitura executa a validação ou verificação de dados para garantir que o conteúdo não tenha sido corrompido ou desconfigurado intencionalmente por terceiros mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="101e6-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="101e6-115">Embora os objetos desse SDK não verifiquem ou validem dados em fluxos arbitrários, vários tipos de fluxos arbitrários têm suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="101e6-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="101e6-116">A tabela a seguir lista os tipos de fluxo arbitrários predefinidos.</span><span class="sxs-lookup"><span data-stu-id="101e6-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="101e6-117">Fluxos de script também têm suporte, mas são discutidos separadamente na seção [comandos de script](script-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="101e6-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="101e6-118">Para obter mais informações sobre como criar tipos personalizados, consulte [fluxos de dados arbitrários personalizados](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="101e6-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="101e6-119">Tipo arbitrário</span><span class="sxs-lookup"><span data-stu-id="101e6-119">Arbitrary type</span></span>                   | <span data-ttu-id="101e6-120">Description</span><span class="sxs-lookup"><span data-stu-id="101e6-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="101e6-121">Fluxos de texto</span><span class="sxs-lookup"><span data-stu-id="101e6-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="101e6-122">Conter cadeias de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="101e6-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="101e6-123">Fluxos de arquivos</span><span class="sxs-lookup"><span data-stu-id="101e6-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="101e6-124">Conter um ou mais arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="101e6-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="101e6-125">Fluxos da Web</span><span class="sxs-lookup"><span data-stu-id="101e6-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="101e6-126">Conter arquivos de dados equivalentes à versão armazenada em cache das páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="101e6-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="101e6-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="101e6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="101e6-128">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="101e6-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="101e6-129">**Fluxos de áudio e vídeo**</span><span class="sxs-lookup"><span data-stu-id="101e6-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="101e6-130">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="101e6-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




