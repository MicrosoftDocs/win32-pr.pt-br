---
title: Considerações para mercados internacionais
description: Considerações para mercados internacionais
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Lojas online do Windows Media Player, mercados internacionais
- lojas online, mercados internacionais
- Digite 1 lojas online, mercados internacionais
- Digite 2 lojas online, mercados internacionais
- mercados internacionais
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761115"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="da3be-113">Considerações para mercados internacionais</span><span class="sxs-lookup"><span data-stu-id="da3be-113">Considerations for International Markets</span></span>

<span data-ttu-id="da3be-114">Se sua empresa cria lojas online para vários mercados, você deve fornecer à Microsoft a URL de um documento do serviceInfo para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="da3be-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="da3be-115">Você pode fazer isso de uma das duas maneiras a seguir:</span><span class="sxs-lookup"><span data-stu-id="da3be-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="da3be-116">Crie um documento do serviceInfo separado para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="da3be-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="da3be-117">Nesse caso, você fornece à Microsoft URLs que apontam para documentos de informações individuais para cada loja online em cada mercado.</span><span class="sxs-lookup"><span data-stu-id="da3be-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="da3be-118">Crie um único documento de informações para todos os mercados.</span><span class="sxs-lookup"><span data-stu-id="da3be-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="da3be-119">Ao fazer isso, você fornece à Microsoft a mesma URL para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="da3be-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="da3be-120">Seu documento do serviceInfo, criado como uma página ASP, pode, então, detectar dinamicamente a localização do usuário com base em parâmetros de cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="da3be-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="da3be-121">O Windows Media Player acrescenta uma cadeia de caracteres de consulta à solicitação de URL do serviceInfo que fornece informações sobre as configurações de localidade e local do usuário.</span><span class="sxs-lookup"><span data-stu-id="da3be-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="da3be-122">Se sua loja online usa essas informações para determinar qual conteúdo exibir, você deve acrescentar esses valores dinamicamente às suas próprias URLs no documento do serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="da3be-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="da3be-123">Essa é a melhor maneira de garantir que as URLs da página da Web sempre conterão os parâmetros esperados.</span><span class="sxs-lookup"><span data-stu-id="da3be-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="da3be-124">Depois de determinar a localidade e a preferência de idioma do usuário, talvez você queira manter essas informações para futuras sessões.</span><span class="sxs-lookup"><span data-stu-id="da3be-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="da3be-125">Você pode fazer isso usando qualquer uma das técnicas que normalmente usaria em uma página da Web, como cookies, ou usando seu objeto COM.</span><span class="sxs-lookup"><span data-stu-id="da3be-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da3be-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da3be-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da3be-127">**Criando o documento do serviceInfo dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="da3be-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="da3be-128">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="da3be-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="da3be-129">**Elemento serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="da3be-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




