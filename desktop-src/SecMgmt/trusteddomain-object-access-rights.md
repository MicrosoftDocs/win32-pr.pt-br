---
description: Lista e explica os direitos de acesso do objeto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Direitos de acesso do objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792663"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="88460-103">Direitos de acesso do objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="88460-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="88460-104">O tipo de objeto [**TrustedDomain**](trusteddomain-object.md) tem os seguintes tipos de acesso:</span><span class="sxs-lookup"><span data-stu-id="88460-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="88460-105">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="88460-105">Access type</span></span>                  | <span data-ttu-id="88460-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="88460-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88460-107">\_nome de \_ domínio de consulta confiável \_</span><span class="sxs-lookup"><span data-stu-id="88460-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="88460-108">Esse tipo de acesso é necessário para consultar o nome do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="88460-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="88460-109">\_controladores de conjuntos confiáveis \_</span><span class="sxs-lookup"><span data-stu-id="88460-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="88460-110">Esse tipo de acesso é necessário para definir a lista de controladores do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="88460-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="88460-111">\_POSIX de consulta confiável \_</span><span class="sxs-lookup"><span data-stu-id="88460-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="88460-112">Esse tipo de acesso é necessário para recuperar o deslocamento de ID POSIX de um domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="88460-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="88460-113">TRUSTed \_ set \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="88460-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="88460-114">Esse tipo de acesso é necessário para definir o deslocamento de ID POSIX de um domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="88460-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="88460-115">Máscaras de acesso genérico</span><span class="sxs-lookup"><span data-stu-id="88460-115">Generic Access Masks</span></span>

<span data-ttu-id="88460-116">Esse tipo de objeto tem os seguintes mapeamentos de acesso genéricos:</span><span class="sxs-lookup"><span data-stu-id="88460-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="88460-117">Tipos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="88460-117">Standard Access Types</span></span>

<span data-ttu-id="88460-118">Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="88460-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="88460-119">Todos os tipos de acesso necessários têm suporte.</span><span class="sxs-lookup"><span data-stu-id="88460-119">All required access types are supported.</span></span> <span data-ttu-id="88460-120">A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:</span><span class="sxs-lookup"><span data-stu-id="88460-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



