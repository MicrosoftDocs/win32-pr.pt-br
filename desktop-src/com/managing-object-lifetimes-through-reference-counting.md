---
title: Gerenciando tempos de vida de objeto por meio de contagem de referência
description: Gerenciando tempos de vida de objeto por meio de contagem de referência
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
# <a name="managing-object-lifetimes-through-reference-counting"></a>Gerenciando tempos de vida de objeto por meio de contagem de referência

Em sistemas de objetos tradicionais, o ciclo de vida dos objetos – ou seja, os problemas que envolvem a criação e a exclusão de objetos — é tratado implicitamente pelo idioma (ou pelo tempo de execução do idioma) ou explicitamente pelos programadores de aplicativos.

Em um sistema em evolução, desconstruído de forma descentralizada composto por componentes reutilizados, não é mais verdade que qualquer cliente, ou mesmo qualquer programador, sempre "sabe" como lidar com o tempo de vida de um componente. Para um cliente com os privilégios de segurança certos, ainda é relativamente fácil criar objetos por meio de uma solicitação simples, mas a exclusão do objeto é totalmente diferente. Não é necessariamente claro quando um objeto não é mais necessário e deve ser excluído. (Os leitores familiarizados com os ambientes de programação de lixo, como Java, podem discordar; no entanto, os objetos Java não abrangem limites de máquina ou até mesmo de processos e, portanto, a coleta de lixo é restrita a objetos que vivem em um espaço de processo único. Além disso, o Java força o uso de uma única linguagem de programação.) Mesmo quando o cliente original é concluído com o objeto, ele não pode simplesmente desligar o objeto, porque algum outro cliente ou clientes ainda podem ter uma referência a ele.

Uma maneira de garantir que um objeto não seja mais necessário é depender inteiramente de um canal de comunicação subjacente para informar o sistema quando todas as conexões com um objeto entre processos ou entre canais tiverem desaparecido. No entanto, os esquemas que usam esse método são inaceitáveis por vários motivos. Um problema é que ele pode exigir uma grande diferença entre o modelo de programação entre processos/várias redes e o modelo de programação de processo único. No modelo de programação entre processos/rede cruzada, o sistema de comunicação forneceria os ganchos necessários para o gerenciamento de tempo de vida do objeto, enquanto no modelo de programação de processo único, os objetos são conectados diretamente sem nenhum canal de comunicação intermediário. Outro problema é que esse esquema também poderia resultar em uma camada de software fornecido pelo sistema que iria interferir no desempenho do componente no caso do processo. Além disso, um mecanismo baseado em monitoramento explícito não tende a ser dimensionado em direção a muitos milhares ou milhões de objetos.

O COM oferece uma abordagem escalonável e distribuída para esse conjunto de problemas. Os clientes informam um objeto quando estão usando-o e quando são concluídos, e os próprios objetos são excluídos quando não são mais necessários. Essa abordagem exige que todos os objetos contem referências a si mesmos. Linguagens de programação como Java, que inerentemente têm seus próprios esquemas de gerenciamento de tempo de vida, como a coleta de lixo, podem usar a contagem de referência de COM para implementar e usar objetos COM internamente, permitindo que o programador Evite lidar com ele.

Assim como um aplicativo deve liberar memória alocada quando essa memória não está mais em uso, um cliente de um objeto é responsável por liberar suas referências para o objeto quando esse objeto não é mais necessário. Em um sistema orientado a objeto, o cliente pode fazer isso apenas dando ao objeto uma instrução para se liberar.

É importante que um objeto seja desalocado quando ele não estiver mais sendo usado. A dificuldade está em determinar quando é apropriado para desalocar um objeto. Isso é fácil com variáveis automáticas (aquelas alocadas na pilha) — elas não podem ser usadas fora do bloco no qual estão declaradas, portanto, o compilador as desaloca quando o final do bloco é atingido. Para objetos COM, que são alocados dinamicamente, cabe aos clientes de um objeto decidir quando eles não precisam mais usar o objeto — especialmente objetos locais ou remotos que podem estar em uso por vários clientes ao mesmo tempo. O objeto deve aguardar até que todos os clientes sejam concluídos com ele antes de se liberar. Como objetos COM são manipulados por meio de ponteiros de interface e podem ser usados por objetos em diferentes processos ou em outros computadores, o sistema não pode controlar os clientes de um objeto.

O método de COM de determinar quando é apropriado desalocar um objeto é a contagem de referência manual. Cada objeto mantém uma contagem de referência que acompanha quantos clientes estão conectados a ele, ou seja, quantos ponteiros existem para qualquer uma de suas interfaces em qualquer cliente.

Para obter mais informações, consulte estes tópicos:

-   [Implementando a contagem de referência](implementing-reference-counting.md)
-   [Regras para gerenciar contagens de referência](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando e implementando IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




