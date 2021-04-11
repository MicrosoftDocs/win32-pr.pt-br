---
title: Removendo atributos de metadados
description: Removendo atributos de metadados
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- SDK do Windows Media Format, removendo atributos de metadados
- Formato de sistema avançado (ASF), removendo atributos de metadados
- ASF (formato de sistemas avançados), removendo atributos de metadados
- metadados, removendo atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365745"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="a04bf-107">Removendo atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="a04bf-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="a04bf-108">Você pode remover um atributo de metadados passando seu índice e o número de fluxo para o método [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) .</span><span class="sxs-lookup"><span data-stu-id="a04bf-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="a04bf-109">A ordem na qual os atributos restantes são indexados após a remoção de um atributo não é alterada; todos os atributos restantes que originalmente tinham um valor de índice maior do que aquele removido têm seus valores de índice reduzidos em um.</span><span class="sxs-lookup"><span data-stu-id="a04bf-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="a04bf-110">Ao remover vários atributos, faça isso em ordem decrescente por índice para evitar ter que calcular o ajuste na indexação.</span><span class="sxs-lookup"><span data-stu-id="a04bf-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="a04bf-111">Para sua conveniência na remoção de valores, o método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) retorna os valores de índice em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="a04bf-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="a04bf-112">Os valores de índice obtidos usando os métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) não são compatíveis com os valores de índice obtidos com o uso dos métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="a04bf-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="a04bf-113">Se você usar os métodos de uma interface para alterar atributos em um arquivo, deverá assumir que qualquer valor de índice recuperado anteriormente da outra interface não será mais válido e deverá ser obtido novamente.</span><span class="sxs-lookup"><span data-stu-id="a04bf-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="a04bf-114">Você deve evitar usar os métodos de **IWMHeaderInfo** , se possível.</span><span class="sxs-lookup"><span data-stu-id="a04bf-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a04bf-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a04bf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a04bf-116">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="a04bf-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




