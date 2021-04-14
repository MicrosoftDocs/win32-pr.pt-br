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
# <a name="private-data-object-access-rights"></a>Direitos de acesso a objeto de dados particulares

Os tipos de acesso desse tipo de objeto são:



| Tipo de acesso          | Descrição                                      |
|----------------------|--------------------------------------------------|
| \_valor da consulta secreta \_ | Esse tipo de acesso é necessário para recuperar um segredo. |
| \_valor do conjunto secreto \_   | Esse tipo de acesso é necessário para modificar um segredo.   |



 

## <a name="generic-access-masks"></a>Máscaras de acesso genérico

Esse tipo de objeto tem os seguintes mapeamentos de acesso genéricos:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipos de acesso padrão:

Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE. Todos os tipos de acesso necessários têm suporte. A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



