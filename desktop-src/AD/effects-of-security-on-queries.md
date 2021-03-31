---
title: Efeitos de segurança na pesquisa
description: A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou propriedades de leitura.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efeitos de segurança na pesquisa Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634968"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="0a6fd-104">Efeitos de segurança na pesquisa</span><span class="sxs-lookup"><span data-stu-id="0a6fd-104">Effects of Security on Searching</span></span>

<span data-ttu-id="0a6fd-105">A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou propriedades de leitura.</span><span class="sxs-lookup"><span data-stu-id="0a6fd-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="0a6fd-106">A ADSI pode não retornar \_ tal \_ propriedade ou nenhum \_ desses erros de \_ objeto, mesmo quando o objeto existir, se você não tiver acesso a atributos de leitura no objeto.</span><span class="sxs-lookup"><span data-stu-id="0a6fd-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="0a6fd-107">Por exemplo, um chamador pode ser capaz de enumerar os objetos filho em um contêiner, pois o chamador tem direitos de conteúdo da lista \_ no contêiner.</span><span class="sxs-lookup"><span data-stu-id="0a6fd-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="0a6fd-108">Mas o mesmo chamador não poderá acessar os objetos enumerados se o chamador não tiver acesso de leitura aos objetos filho.</span><span class="sxs-lookup"><span data-stu-id="0a6fd-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="0a6fd-109">Nesse caso, uma consulta para um objeto filho pode não retornar nenhum \_ objeto desse tipo, \_ embora o chamador tenha enumerado com êxito o objeto.</span><span class="sxs-lookup"><span data-stu-id="0a6fd-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="0a6fd-110">Se o chamador não tiver direitos suficientes, os códigos de retorno a seguir poderão ser retornados:</span><span class="sxs-lookup"><span data-stu-id="0a6fd-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="0a6fd-111">\_objeto de \_ \_ domínio inválido \_ do E ADS</span><span class="sxs-lookup"><span data-stu-id="0a6fd-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="0a6fd-112">\_Propriedade E \_ ADS \_ sem \_ suporte</span><span class="sxs-lookup"><span data-stu-id="0a6fd-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="0a6fd-113">\_Propriedade E \_ ADS \_ não \_ encontrada</span><span class="sxs-lookup"><span data-stu-id="0a6fd-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




