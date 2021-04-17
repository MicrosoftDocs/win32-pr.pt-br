---
description: O atributo de sincronização é uma propriedade declarativa que especifica que tipo de sincronização você deseja que os componentes tenham quando são ativados.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Valores de atributo de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370412"
---
# <a name="synchronization-attribute-values"></a>Valores de atributo de sincronização

O atributo de sincronização é uma propriedade declarativa que especifica que tipo de sincronização você deseja que os componentes tenham quando são ativados. Quando você inclui o atributo de sincronização, o COM+ manipula os detalhes de sincronização em seu nome; Você não precisa fazer nenhuma outra chamada.

Dependendo de seus requisitos, um objeto pode compartilhar a sincronização de seu chamador, exigir uma nova sincronização ou operar sem sincronização.

O COM+ fornece os seguintes valores de atributo de sincronização:

-   **Desabilitado.** Quando você desabilita o atributo de sincronização, o COM+ ignora os requisitos de sincronização do componente para determinar o contexto do objeto. Como resultado, o objeto pode ou não compartilhar o contexto (e a sincronização) do chamador.

    Em geral, você deve usar esse valor de atributo quando souber que o componente nunca acessa um Gerenciador de recursos. Ao migrar componentes COM para COM+, você deve desabilitar o atributo de sincronização para manter o mesmo comportamento que o componente COM não configurado. Um componente não configurado é um componente COM que não foi instalado em um aplicativo COM+.

-   **Sem suporte.** Um objeto com esse valor nunca participa da sincronização, independentemente do status de seu chamador. Essa configuração está disponível somente para componentes que não são transacionais e não usam o serviço de [ativação JIT (just-in-time) do com+](com--just-in-time-activation.md) .

-   **Porta.** Um objeto com esse valor participa da sincronização, se existir. Você declara esse valor quando deseja que um objeto Compartilhe na sincronização de seu chamador, mas não requer a sincronização de seu próprio.

    Um bom motivo para definir o atributo de sincronização como com suporte é que essa configuração pode ser menos dispendiosa em termos de recursos do sistema. No entanto, é mais difícil escrever seu componente devido à necessidade de protegê-lo de chamadas simultâneas. A implicação de definir o atributo de sincronização como com suporte é que, em determinadas circunstâncias, uma instância do seu objeto pode ser criada de forma que não seja sincronizada. Se o modelo de Threading do componente for gratuito ou ambos, você precisará proteger os dados da instância com algum tipo de mecanismo de bloqueio. Se o modelo de Threading for Apartment (STA), você não precisará proteger os dados da instância.

-   **Necessário.** Quando você define esse atributo, o COM+ garante que todos os objetos criados a partir do componente serão sincronizados. Na verdade, sempre que o COM+ cria uma instância do seu componente, ele verifica se há apenas um thread passando por essa instância por vez.

    À medida que o COM+ ativa um objeto, ele examina o status de sincronização de seu chamador. Se o chamador for sincronizado, o COM+ fluirá o limite de sincronização do chamador para incluir o novo objeto. Caso contrário, o COM+ iniciará a sincronização.

-   **Requer novo.** Um objeto com esse valor deve participar de uma nova sincronização, onde o COM+ gerencia contextos e Apartments em nome de todos os componentes envolvidos na chamada. O COM+ inicia automaticamente uma nova sincronização, que é distinta da sincronização do chamador.

    Um bom motivo para definir seu atributo de sincronização como requer novo é que essa configuração permite que você faça chamadas externas para uma instância do seu componente com mais eficiência. No entanto, ele também faz chamadas entre o objeto e o objeto que o criou mais caro em termos de recursos do sistema.

    Por exemplo, suponha um caso em que o objeto e seu objeto criador compartilhem o mesmo limite de sincronização. Se o cliente A chamar o objeto Creator e o cliente B chamar o objeto, a segunda chamada terá de aguardar até que a primeira chamada seja concluída. Se você definir requer novo, o objeto é criado em um limite de sincronização separado. Nesse caso, as chamadas de outros objetos podem ser processadas ao mesmo tempo. No entanto, as chamadas do objeto Creator para seu objeto exigem mais recursos do sistema porque devem cruzar limites de sincronização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o atributo de sincronização](setting-the-synchronization-attribute.md)
</dt> <dt>

[Dependências de sincronização](synchronization-dependencies.md)
</dt> </dl>

 

 



