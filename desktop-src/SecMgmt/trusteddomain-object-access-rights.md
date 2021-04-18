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
# <a name="trusteddomain-object-access-rights"></a>Direitos de acesso do objeto TrustedDomain

O tipo de objeto [**TrustedDomain**](trusteddomain-object.md) tem os seguintes tipos de acesso:



| Tipo de acesso                  | Descrição                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| \_nome de \_ domínio de consulta confiável \_ | Esse tipo de acesso é necessário para consultar o nome do domínio confiável.              |
| \_controladores de conjuntos confiáveis \_    | Esse tipo de acesso é necessário para definir a lista de controladores do domínio confiável. |
| \_POSIX de consulta confiável \_        | Esse tipo de acesso é necessário para recuperar o deslocamento de ID POSIX de um domínio confiável.  |
| TRUSTed \_ set \_ POSIX          | Esse tipo de acesso é necessário para definir o deslocamento de ID POSIX de um domínio confiável.       |



 

## <a name="generic-access-masks"></a>Máscaras de acesso genérico

Esse tipo de objeto tem os seguintes mapeamentos de acesso genéricos:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Tipos de acesso padrão

Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE. Todos os tipos de acesso necessários têm suporte. A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



