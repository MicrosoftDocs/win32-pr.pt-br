---
description: Interfaces de streaming de multimídia base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de streaming de multimídia base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930214"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="205dc-103">Interfaces de streaming de multimídia base</span><span class="sxs-lookup"><span data-stu-id="205dc-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="205dc-104">Essas APIs são preteridas.</span><span class="sxs-lookup"><span data-stu-id="205dc-104">These APIs are deprecated.</span></span> <span data-ttu-id="205dc-105">Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="205dc-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="205dc-106">As interfaces de streaming de multimídia base fornecem uma maneira programática de acessar fluxos de multimídia.</span><span class="sxs-lookup"><span data-stu-id="205dc-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="205dc-107">No entanto, usar uma interface base para acessar um tipo específico de dados pode limitar a quantidade de controle que você tem sobre os dados; portanto, os desenvolvedores de mídia devem criar versões derivadas dessas interfaces que fornecem um controle mais poderoso sobre os recursos exclusivos de seu tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="205dc-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="205dc-108">Interface</span><span class="sxs-lookup"><span data-stu-id="205dc-108">Interface</span></span>                                      | <span data-ttu-id="205dc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="205dc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="205dc-110">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="205dc-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="205dc-111">Define como acessar o objeto de fluxo multimídia de nível mais alto; Este objeto contém e fornece acesso a outros objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="205dc-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="205dc-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) tem métodos que enumeram ou recuperam fluxos específicos, bem como verificam a duração total do fluxo e buscam dentro do fluxo.</span><span class="sxs-lookup"><span data-stu-id="205dc-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="205dc-113">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="205dc-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="205dc-114">Define um objeto de fluxo genérico.</span><span class="sxs-lookup"><span data-stu-id="205dc-114">Defines a generic stream object.</span></span> <span data-ttu-id="205dc-115">Use seus métodos para recuperar um ponteiro para o fluxo, obter informações sobre o fluxo e criar exemplos a partir dos dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="205dc-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="205dc-116">Você também pode criar amostras de fluxo compartilhado, que vários fluxos podem acessar sem duplicar os dados do exemplo.</span><span class="sxs-lookup"><span data-stu-id="205dc-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="205dc-117">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="205dc-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="205dc-118">Controla o comportamento de um exemplo de fluxo específico.</span><span class="sxs-lookup"><span data-stu-id="205dc-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="205dc-119">Você pode recuperar o fluxo que criou o exemplo, verificar as horas de início e de término e o status de conclusão do exemplo e executar uma função definida pelo usuário no próprio exemplo (por meio do método [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ).</span><span class="sxs-lookup"><span data-stu-id="205dc-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="205dc-120">Normalmente, o método Update processa os dados de exemplo de maneira apropriada, como a renderização de dados de vídeo ou reprodução de dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="205dc-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="205dc-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="205dc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="205dc-122">Lista de interfaces de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="205dc-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



