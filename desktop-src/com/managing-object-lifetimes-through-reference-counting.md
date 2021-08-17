---
title: Gerenciando os tempos de vida do objeto por meio da contagem de referência
description: Gerenciando os tempos de vida do objeto por meio da contagem de referência
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f2c75352eef5680eb9a4d8367f76f88c19138dd834b71068740bee18f2315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310556"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Gerenciando os tempos de vida do objeto por meio da contagem de referência

Em sistemas de objetos tradicionais, o ciclo de vida de objetos ( ou seja, os problemas relacionados à criação e exclusão de objetos ) é tratado implicitamente pela linguagem (ou pelo tempo de run time) ou explicitamente por programadores de aplicativos.

Em um sistema em evolução e construído de forma descentralizada, com componentes reutilizados, não é mais verdade que qualquer cliente, ou até mesmo qualquer programador, sempre "sabe" como lidar com o tempo de vida de um componente. Para um cliente com os privilégios de segurança certos, ainda é relativamente fácil criar objetos por meio de uma solicitação simples, mas a exclusão de objeto é totalmente outra questão. Não é necessariamente claro quando um objeto não é mais necessário e deve ser excluído. (Leitores familiarizados com ambientes de programação coletados pelo lixo, como Java, podem não concordar; no entanto, os objetos Java não abrangem os limites do computador ou até mesmo do processo e, portanto, a coleta de lixo é restrita a objetos que residem em um espaço de processo único. Além disso, o Java força o uso de uma única linguagem de programação.) Mesmo quando o cliente original é feito com o objeto , ele não pode simplesmente desligar o objeto, porque alguns outros clientes ou clientes ainda podem ter uma referência a ele.

Uma maneira de garantir que um objeto não seja mais necessário é depender inteiramente de um canal de comunicação subjacente para informar o sistema quando todas as conexões com um objeto entre processos ou entre canais desaparecerem. No entanto, os esquemas que usam esse método são inaceitáveis por vários motivos. Um problema é que isso pode exigir uma grande diferença entre o modelo de programação entre processos/redes e o modelo de programação de processo único. No modelo de programação entre processos/entre redes, o sistema de comunicação forneceria os ganchos necessários para o gerenciamento de tempo de vida do objeto, enquanto no modelo de programação de processo único, os objetos são conectados diretamente sem nenhum canal de comunicação intermediária. Outro problema é que esse esquema também pode resultar em uma camada de software fornecido pelo sistema que interferiria no desempenho do componente no caso em processo. Além disso, um mecanismo baseado no monitoramento explícito não tende a ser dimensionado para muitos milhares ou milhões de objetos.

O COM oferece uma abordagem escalonável e distribuída para esse conjunto de problemas. Os clientes contam a um objeto quando o estão usando e quando são feitos e os objetos se excluem quando não são mais necessários. Essa abordagem determina que todos os objetos contam referências a si mesmos. Linguagens de programação como Java, que inerentemente têm seus próprios esquemas de gerenciamento de tempo de vida, como coleta de lixo, podem usar a contagem de referência do COM para implementar e usar objetos COM internamente, permitindo que o programador evite lidar com ele.

Assim como um aplicativo deve liberar memória alocada depois que a memória não está mais em uso, um cliente de um objeto é responsável por liberar suas referências ao objeto quando esse objeto não é mais necessário. Em um sistema orientado a objeto, o cliente pode fazer isso apenas dando ao objeto uma instrução para se liberar.

É importante que um objeto seja desaloqueado quando ele não estiver mais sendo usado. A dificuldade está em determinar quando é apropriado desalocar um objeto. Isso é fácil com variáveis automáticas (alocadas na pilha) – elas não podem ser usadas fora do bloco no qual são declaradas, portanto, o compilador as desaloca quando o final do bloco é atingido. Para objetos COM, que são alocados dinamicamente, é responsabilidade dos clientes de um objeto decidir quando eles não precisam mais usar o objeto , especialmente objetos locais ou remotos que podem estar em uso por vários clientes ao mesmo tempo. O objeto deve aguardar até que todos os clientes sejam concluídos antes de se liberarem. Como os objetos COM são manipulados por meio de ponteiros de interface e podem ser usados por objetos em processos diferentes ou em outros máquinas, o sistema não pode controlar os clientes de um objeto.

O método de COM para determinar quando é apropriado desalocar um objeto é a contagem de referência manual. Cada objeto mantém uma contagem de referência que rastreia quantos clientes estão conectados a ele, ou seja, quantos ponteiros existem para qualquer uma de suas interfaces em qualquer cliente.

Para obter mais informações, consulte estes tópicos:

-   [Implementando a contagem de referência](implementing-reference-counting.md)
-   [Regras para gerenciar contagens de referência](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando e implementando IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




