---
description: Segurança de aplicativos de várias camadas
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Segurança de aplicativos de várias camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070465"
---
# <a name="multi-tier-application-security"></a>Segurança de aplicativos de várias camadas

Você pode enfrentar opções difíceis de decidir precisamente onde impor a segurança em um aplicativo baseado em componentes de várias camadas: no banco de dados? Na camada intermediária? Nos componentes? Outro lugar? Parte? À medida que os mecanismos de segurança aumentam em número e complexidade, os declínios de desempenho e o comportamento do aplicativo se tornam menos previsíveis. No entanto, você deve garantir que os dados estejam protegidos, que as regras de negócio sejam seguidas e que a atividade significativa seja registrada e ainda ter seu aplicativo funcionando para clientes como pretendido. Você deve ter certeza de que cada caminho de cliente por meio de seu aplicativo está correto e que os pontos de verificação de segurança que você tem em vigor serão suficientes.

A decisão mais difícil é geralmente se a segurança deve ser imposta no banco de dados. Historicamente, é aí que a segurança é mais rígida, pois é percebida como um reino que precisa ser verdadeiramente seguro, e os administradores de banco de dados são muito relutantes em confiar em outra pessoa para impor a segurança para eles. Mas a imposição da segurança no banco de dados pode ser bastante cara e difícil de dimensionar, o que é precisamente o ponto de escrever aplicativos de várias camadas em primeiro lugar.

A regra geral a seguir com aplicativos de várias camadas escalonáveis usando COM+ é que, sempre que possível, você deve impor segurança detalhada no aplicativo COM+ na camada intermediária. Isso permite que você aproveite totalmente os serviços escalonáveis fornecidos pelo COM+. Autentique no banco de dados somente quando for absolutamente necessário, e avalie totalmente as implicações de desempenho de fazer isso.

Para obter uma discussão sobre problemas a serem considerados ao decidir onde executar verificações de segurança, consulte [decidindo onde impor a segurança](deciding-where-to-enforce-security.md).

Para obter uma discussão sobre alguns cenários básicos de proteção de aplicativos de várias camadas, consulte [cenários básicos para proteger dados em aplicativos de várias camadas](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



