---
title: Recuperando atributos de metadados
description: Recuperando atributos de metadados
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- SDK do Windows Media Format, recuperando atributos de metadados
- ASF (Advanced Systems Format), recuperando atributos de metadados
- ASF (formato de sistemas avançados), recuperando atributos de metadados
- metadados, recuperando atributos
- fluxos, recuperando atributos de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007076"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="b4a1b-108">Recuperando atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="b4a1b-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="b4a1b-109">Para recuperar um atributo de um cabeçalho de arquivo, você deve saber o número de fluxo e o índice do atributo.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="b4a1b-110">Você pode usar o método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obter os índices de todos os atributos com o mesmo nome ou todos os índices no mesmo idioma.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="b4a1b-111">Como os outros métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), o **GetAttributeIndices** lida com um único fluxo ou com todos os atributos de nível de arquivo usando o fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="b4a1b-112">Você pode usar 0xFFFF para o número de fluxo para obter índices globais que correspondem aos seus critérios em todo o arquivo, independentemente do número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="b4a1b-113">Quando você souber o índice do atributo que deseja recuperar, chame [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="b4a1b-114">Você precisa fazer duas chamadas para **GetAttributeByIndexEx** para cada atributo recuperado.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="b4a1b-115">Na primeira chamada, passe **NULL** para os ponteiros de nome e buffer de dados para obter o tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="b4a1b-116">Em seguida, aloque os buffers do tamanho indicado e faça a segunda chamada para recuperar o nome e os dados.</span><span class="sxs-lookup"><span data-stu-id="b4a1b-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="b4a1b-117">Por exemplo, código mostrando como recuperar atributos de metadados, consulte [para recuperar todos os metadados em um arquivo](to-retrieve-all-metadata-in-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="b4a1b-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4a1b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4a1b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a1b-119">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="b4a1b-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




