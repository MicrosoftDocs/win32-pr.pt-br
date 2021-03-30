---
title: O cache de atributo ADSI
description: O modelo de objeto ADSI fornece um cache de atributos do lado do cliente para cada objeto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- O ADSI do cache de atributo ADSI
- ADSI, usando, acessando e manipulando dados com ADSI, cache de atributos
- atributos ADSI, cache de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634860"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="f59ae-106">O cache de atributo ADSI</span><span class="sxs-lookup"><span data-stu-id="f59ae-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="f59ae-107">O modelo de objeto ADSI fornece um cache de atributos do lado do cliente para cada objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="f59ae-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="f59ae-108">O cache de atributo é comparável a uma tabela na memória que contém os nomes e valores da maioria dos atributos de objeto que foram baixados.</span><span class="sxs-lookup"><span data-stu-id="f59ae-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="f59ae-109">Alguns atributos, como atributos operacionais, não são armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="f59ae-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="f59ae-110">A ADSI usa o cache de propriedades para aprimorar o desempenho da manipulação de atributos e adicionar capacidade de transacionamento para operações de leitura e gravação de atributo.</span><span class="sxs-lookup"><span data-stu-id="f59ae-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="f59ae-111">Esse recurso é essencial para clientes escritos em linguagens que não têm um mecanismo de envio em lote nativo para a configuração de atributos, como o sistema de desenvolvimento Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f59ae-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="f59ae-112">Sem o cache de propriedades ADSI, esses clientes teriam que acessar o servidor sempre que um atributo for lido ou gravado.</span><span class="sxs-lookup"><span data-stu-id="f59ae-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="f59ae-113">Quando um objeto é criado ou associado primeiro a, o cache de propriedades do objeto está vazio.</span><span class="sxs-lookup"><span data-stu-id="f59ae-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="f59ae-114">Quando o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é chamado, a ADSI carrega os atributos solicitados para o objeto do serviço de diretório subjacente no cache local.</span><span class="sxs-lookup"><span data-stu-id="f59ae-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="f59ae-115">Quando um valor de atributo específico é lido e o cache está vazio, a ADSI faz uma chamada implícita para o método **IADs:: GetInfo** .</span><span class="sxs-lookup"><span data-stu-id="f59ae-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="f59ae-116">Quando o cache é preenchido, todas as operações de leitura de atributo funcionam apenas no conteúdo do cache.</span><span class="sxs-lookup"><span data-stu-id="f59ae-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="f59ae-117">Quando um valor de atributo é gravado, o novo valor é armazenado no cache local até que o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f59ae-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="f59ae-118">Quando o método **IADs:: setinfo** é chamado, os atributos no cache são confirmados no serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="f59ae-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="f59ae-119">Depois que o método **IADs:: setinfo** é chamado, os valores permanecem no cache até que sejam explicitamente atualizados com outra chamada para o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="f59ae-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f59ae-120">O método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) deve ser usado com cuidado porque esse método sempre substituirá os valores de atributo no cache do serviço de diretório subjacente, mesmo que o valor em cache tenha sido alterado.</span><span class="sxs-lookup"><span data-stu-id="f59ae-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="f59ae-121">Ou seja, ele substituirá os valores de atributo que foram alterados no cache, mas não confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="f59ae-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="f59ae-122">A figura a seguir mostra os diferentes métodos usados para operar no cache.</span><span class="sxs-lookup"><span data-stu-id="f59ae-122">The following figure shows the different methods used to operate on the cache.</span></span>

![cache de atributo ADSI](images/ds2propc.png)

 

 




