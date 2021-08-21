---
title: Controle de acesso e operações de leitura
description: A segurança é um filtro implícito para pesquisar, enumerar contêineres ou ler propriedades.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Controle de acesso e AD de operações de leitura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f11dfd0b8d65bf0346f66fa4d7b959cb2893718bef44303d3774b19c29a97ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025496"
---
# <a name="access-control-and-read-operations"></a>Controle de acesso e operações de leitura

A segurança é um filtro implícito para pesquisar, enumerar contêineres ou ler propriedades. Se você não tiver os direitos de acesso necessários, as tentativas de listar objetos ou ler propriedades poderão falhar com os seguintes códigos de erro até mesmo pensando que o objeto ou a propriedade existe:

-   **E \_ ADS OBJETO DE DOMÍNIO \_ \_ \_ INVÁLIDO**
-   **PROPRIEDADE \_ E ADS SEM \_ \_ \_ SUPORTE**
-   **PROPRIEDADE \_ E ADS NÃO \_ \_ \_ ENCONTRADA**

Esteja ciente de que um chamador com **acesso ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST** a um contêiner pode enumerar os objetos filho no contêiner. Mas uma tentativa de acessar um objeto filho ainda poderá falhar com um erro como **E \_ ADS UNKNOWN \_ \_ OBJECT** se o chamador não tiver acesso ADS **RIGHT \_ \_ ACTRL \_ DS LIST \_ \_ OBJECT** ao objeto filho.

O impacto da segurança em operações de leitura não é necessariamente manifestado como um erro. Por exemplo, uma operação de pesquisa pode ser bem-sucedida, mas os resultados da pesquisa não incluem objetos ou propriedades às quais o chamador não tem acesso.

 

 




