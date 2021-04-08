---
title: Controle de acesso e operações de leitura
description: Segurança é um filtro implícito para pesquisar, enumerar contêineres ou propriedades de leitura.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Controle de acesso e operações de leitura AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004821"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="f2dc9-104">Controle de acesso e operações de leitura</span><span class="sxs-lookup"><span data-stu-id="f2dc9-104">Access Control and Read Operations</span></span>

<span data-ttu-id="f2dc9-105">Segurança é um filtro implícito para pesquisar, enumerar contêineres ou propriedades de leitura.</span><span class="sxs-lookup"><span data-stu-id="f2dc9-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="f2dc9-106">Se você não tiver os direitos de acesso necessários, as tentativas de listar objetos ou propriedades de leitura poderão falhar com os seguintes códigos de erro até mesmo pensar que o objeto ou a propriedade exista:</span><span class="sxs-lookup"><span data-stu-id="f2dc9-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="f2dc9-107">**\_objeto de \_ \_ domínio inválido \_ do E ADS**</span><span class="sxs-lookup"><span data-stu-id="f2dc9-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="f2dc9-108">**\_Propriedade E \_ ADS \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="f2dc9-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="f2dc9-109">**\_Propriedade E \_ ADS \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="f2dc9-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="f2dc9-110">Lembre-se de que um chamador com **ADS \_ Right \_ ACTRL \_ DS \_ listar** acesso a um contêiner pode enumerar os objetos filho no contêiner.</span><span class="sxs-lookup"><span data-stu-id="f2dc9-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="f2dc9-111">Mas uma tentativa de acessar um objeto filho ainda pode falhar com um erro, por exemplo, **E o \_ objeto de anúncio \_ desconhecido \_** se o chamador não tiver o direito de acesso ao **\_ \_ \_ \_ \_ objeto de lista do AD ACTRL** ao objeto filho.</span><span class="sxs-lookup"><span data-stu-id="f2dc9-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="f2dc9-112">O impacto da segurança nas operações de leitura não é necessariamente manifestado como um erro.</span><span class="sxs-lookup"><span data-stu-id="f2dc9-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="f2dc9-113">Por exemplo, uma operação de pesquisa pode ser realizada com sucesso, mas os resultados da pesquisa não incluem objetos ou Propriedades às quais o chamador não tem acesso.</span><span class="sxs-lookup"><span data-stu-id="f2dc9-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




