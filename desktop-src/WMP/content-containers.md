---
title: Contêineres de conteúdo
description: Contêineres de conteúdo
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Lojas online do Windows Media Player, contêineres de conteúdo
- lojas online, contêineres de conteúdo
- Digite 1 lojas online, contêineres de conteúdo
- Lojas online do Windows Media Player, interface IWMPContentContainer
- lojas online, interface IWMPContentContainer
- Digite 1 lojas online, interface IWMPContentContainer
- Windows Media Player, contêineres de conteúdo
- Windows Media Player, interface IWMPContentContainer
- contêineres de conteúdo
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105759730"
---
# <a name="content-containers"></a><span data-ttu-id="997c4-113">Contêineres de conteúdo</span><span class="sxs-lookup"><span data-stu-id="997c4-113">Content Containers</span></span>

<span data-ttu-id="997c4-114">O Windows Media Player usa contêineres de conteúdo para representar o conteúdo de mídia digital em um download de assinatura ou transação de compra.</span><span class="sxs-lookup"><span data-stu-id="997c4-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="997c4-115">Um contêiner de conteúdo é representado pela interface **IWMPContentContainer** .</span><span class="sxs-lookup"><span data-stu-id="997c4-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="997c4-116">Um contêiner de conteúdo pode conter uma lista de conteúdo relacionado, como um álbum ou um conjunto de itens de conteúdo não relacionados ou *faixas*.</span><span class="sxs-lookup"><span data-stu-id="997c4-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="997c4-117">Você pode usar a interface **IWMPContentContainer** para enumerar as faixas do contêiner de conteúdo e recuperar o preço de cada faixa. Você também pode recuperar informações sobre o próprio contêiner de conteúdo, como a ID do contêiner, o tipo de conteúdo no contêiner e o preço total para as faixas no contêiner (que podem ser diferentes da soma dos preços das faixas individuais, como no caso de uma compra de álbum).</span><span class="sxs-lookup"><span data-stu-id="997c4-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="997c4-118">Para fornecer um mecanismo para empacotar vários contêineres de conteúdo em um único objeto, o Windows Media Player dá suporte à interface **IWMPContentContainerList** .</span><span class="sxs-lookup"><span data-stu-id="997c4-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="997c4-119">**IWMPContentContainerList** fornece métodos para enumerar e recuperar os contêineres de conteúdo na lista.</span><span class="sxs-lookup"><span data-stu-id="997c4-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="997c4-120">Para descobrir se a lista de contêineres de conteúdo representa uma compra ou um download de assinatura, chame [IWMPContentContainerList:: Gettransactiontype](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) para recuperar um valor de [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .</span><span class="sxs-lookup"><span data-stu-id="997c4-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="997c4-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="997c4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="997c4-122">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="997c4-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="997c4-123">**Interface IWMPContentContainer**</span><span class="sxs-lookup"><span data-stu-id="997c4-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="997c4-124">**Interface IWMPContentContainerList**</span><span class="sxs-lookup"><span data-stu-id="997c4-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




