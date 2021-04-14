---
description: Lista e explica os direitos de acesso do objeto de dados particular.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Direitos de acesso a objeto de dados particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461024"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="afb9e-103">Direitos de acesso a objeto de dados particulares</span><span class="sxs-lookup"><span data-stu-id="afb9e-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="afb9e-104">Os tipos de acesso desse tipo de objeto são:</span><span class="sxs-lookup"><span data-stu-id="afb9e-104">The access types of this object type are:</span></span>



| <span data-ttu-id="afb9e-105">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="afb9e-105">Access type</span></span>          | <span data-ttu-id="afb9e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="afb9e-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="afb9e-107">\_valor da consulta secreta \_</span><span class="sxs-lookup"><span data-stu-id="afb9e-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="afb9e-108">Esse tipo de acesso é necessário para recuperar um segredo.</span><span class="sxs-lookup"><span data-stu-id="afb9e-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="afb9e-109">\_valor do conjunto secreto \_</span><span class="sxs-lookup"><span data-stu-id="afb9e-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="afb9e-110">Esse tipo de acesso é necessário para modificar um segredo.</span><span class="sxs-lookup"><span data-stu-id="afb9e-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="afb9e-111">Máscaras de acesso genérico</span><span class="sxs-lookup"><span data-stu-id="afb9e-111">Generic Access Masks</span></span>

<span data-ttu-id="afb9e-112">Esse tipo de objeto tem os seguintes mapeamentos de acesso genéricos:</span><span class="sxs-lookup"><span data-stu-id="afb9e-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="afb9e-113">Tipos de acesso padrão:</span><span class="sxs-lookup"><span data-stu-id="afb9e-113">Standard Access Types:</span></span>

<span data-ttu-id="afb9e-114">Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="afb9e-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="afb9e-115">Todos os tipos de acesso necessários têm suporte.</span><span class="sxs-lookup"><span data-stu-id="afb9e-115">All required access types are supported.</span></span> <span data-ttu-id="afb9e-116">A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:</span><span class="sxs-lookup"><span data-stu-id="afb9e-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



