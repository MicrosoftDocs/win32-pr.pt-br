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
# <a name="access-control-and-read-operations"></a>Controle de acesso e operações de leitura

Segurança é um filtro implícito para pesquisar, enumerar contêineres ou propriedades de leitura. Se você não tiver os direitos de acesso necessários, as tentativas de listar objetos ou propriedades de leitura poderão falhar com os seguintes códigos de erro até mesmo pensar que o objeto ou a propriedade exista:

-   **\_objeto de \_ \_ domínio inválido \_ do E ADS**
-   **\_Propriedade E \_ ADS \_ sem \_ suporte**
-   **\_Propriedade E \_ ADS \_ não \_ encontrada**

Lembre-se de que um chamador com **ADS \_ Right \_ ACTRL \_ DS \_ listar** acesso a um contêiner pode enumerar os objetos filho no contêiner. Mas uma tentativa de acessar um objeto filho ainda pode falhar com um erro, por exemplo, **E o \_ objeto de anúncio \_ desconhecido \_** se o chamador não tiver o direito de acesso ao **\_ \_ \_ \_ \_ objeto de lista do AD ACTRL** ao objeto filho.

O impacto da segurança nas operações de leitura não é necessariamente manifestado como um erro. Por exemplo, uma operação de pesquisa pode ser realizada com sucesso, mas os resultados da pesquisa não incluem objetos ou Propriedades às quais o chamador não tem acesso.

 

 




