---
description: A confiabilidade de um certificado digital é estabelecida usando uma hierarquia de confiança.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Hierarquia de confiança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485c721493a93c7ea55b1993345e8168ccab319b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829533"
---
# <a name="hierarchy-of-trust"></a>Hierarquia de confiança

Para que os [*certificados digitais*](../secgloss/c-gly.md) sejam efetivos, os usuários de certificados devem ter um alto nível de confiança neles. Há casos em que um usuário não confia no emissor de um certificado. Isso pode acontecer se o usuário do certificado nunca ouviu falar da [*autoridade de certificação*](../secgloss/c-gly.md) e, portanto, estiver desconfortável com a aceitação de um certificado desse emissor no valor de face. Esse problema é abordado no processo de certificação por uma hierarquia de confiança.

Uma hierarquia de confiança começa com pelo menos uma autoridade de certificação que é confiável para todas as entidades na cadeia de certificados. Isso pode ser um administrador de autoridade de certificação interna ou uma empresa externa ou organização especializada na verificação de identidades e emissão de certificados. Essa autoridade é chamada de [*autoridade raiz*](../secgloss/r-gly.md). Em seguida, a autoridade raiz certifica outras autoridades de certificação, chamadas de autoridades de certificação de primeira camada, que podem emitir certificados e também certificar autoridades de certificação adicionais ou de segunda camada. Essa situação é mostrada na ilustração a seguir.

![hierarquia de confiança](images/trust.png)

A identidade da autoridade de certificação que emite um certificado é parte de um certificado. Essa autoridade de certificação é chamada de emissor do certificado. Quando o emissor de um certificado é uma autoridade de certificação de camada 1 ou 2, o receptor desse certificado pode determinar se o emissor do certificado é certificado como uma autoridade de certificação válida por uma autoridade de certificação em um nível acima dele, e se a autoridade de certificação de nível superior é certificada como uma autoridade de certificação válida, ainda uma autoridade de certificação de nível superior até que seja determinado que existe uma cadeia de confiança entre a autoridade de certificação de nível mais baixa e a raiz autoridade de certificação.

Por exemplo, na ilustração anterior, pode ser verificado que a CA \# 4 foi certificada como uma autoridade de certificação pela CA \# 1, e que \# a CA 1 foi certificada como uma autoridade de certificação pela CA raiz. Assim, quando um certificado de uma autoridade de certificação de nível inferior é passado junto com a mensagem criptografada, as informações sobre todos os certificados em sua cadeia de confiança até a raiz são passadas junto com ela.

A ilustração e a descrição que acabamos de ver são conceituais. No mundo real, a situação da autoridade de certificação está evoluindo e nenhuma autoridade raiz única foi estabelecida ou aceita. A curto prazo, as ilhas de autoridade serão desenvolvidas conforme mostrado na ilustração a seguir.

![Ilhas de autoridade em uma hierarquia de confiança](images/trust2.png)

No tempo, as ilhas raiz 1 e raiz 2 na ilustração podem se tornar CAs da camada 1 para uma única autoridade de certificação raiz. Nesse ponto, a situação teria novamente uma única autoridade raiz. Ele continua sendo visto apenas como a imagem real evoluirá.

 

 
