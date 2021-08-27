---
description: 'A segunda etapa em um processo de design de aplicativo COM+ é dividir o modelo conceitual em camadas lógicas da arquitetura de três camadas: a camada de apresentação ou os serviços de usuário; a camada intermediária ou os serviços corporativos; e a camada de dados ou serviços de dados. Se você não estiver familiarizado com a arquitetura de três camadas, consulte usando um modelo de arquitetura de Three-Tier.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'O modelo lógico: definição e planejamento de aplicativos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19a493ebdacebac27edd291e747b5c42612f5fffd3ac7ea489f99b41de272b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120326"
---
# <a name="the-logical-model-application-definition-and-planning"></a>O modelo lógico: definição e planejamento de aplicativos

A segunda etapa em um processo de design de aplicativo COM+ é dividir o modelo conceitual em camadas lógicas da arquitetura de três camadas: a *camada de apresentação* ou os serviços de usuário; a *camada intermediária* ou os serviços corporativos; e a *camada de dados* ou serviços de dados. Se você não estiver familiarizado com a arquitetura de três camadas, consulte [usando um modelo de arquitetura de Three-Tier](using-a-three-tier-architecture-model.md).

Inicie esse processo examinando o modelo conceitual para substantivos e verbos. Os substantivos geralmente podem ser convertidos em objetos comerciais (classes) e os verbos associados a eles podem ser convertidos em ações (métodos das classes). Embora possa ser difícil definir todos os substantivos como objetos comerciais, as omissões ou os erros se tornarão óbvios no momento em que você concluir o modelo lógico.

A maioria dos objetos comerciais acabará na camada de serviços corporativos, com os objetos restantes divididos entre objetos de interface do usuário na camada de serviços de usuário e objetos de dados na camada de serviços de dados. Ao criar um modelo lógico usando a arquitetura de três camadas, tenha em mente o seguinte:

-   Alguns dos substantivos no design conceitual não representarão os dados físicos reais, mas podem representar uma ação no sistema ou na função de um objeto comercial no sistema. Um objeto comercial também pode ser um serviço que executa algum tipo de controle do sistema, como uma ID de logon para segurança.
-   Evite criar objetos comerciais vagos por meio da "leitura entre as linhas" no [modelo conceitual](the-conceptual-model--application-requirements.md). Esses objetos comerciais podem não estar corretos e você deve considerá-los cuidadosamente antes de incluí-los no modelo lógico. Se eles aparecerem corretos, adicione-os ao modelo conceitual explicitamente.
-   Evite criar objetos comerciais que expressem as mesmas informações ou funções; a duplicação pode ser dispendiosa em termos de velocidade e desempenho do aplicativo.
-   Determinar dependências de objeto. Alguns substantivos no modelo conceitual podem ser simplesmente atributos de outros objetos comerciais. Decida se o atributo pode existir de forma independente. Nesse caso, ele deve se tornar seu próprio objeto de negócios; caso contrário, ele deve ser combinado com o objeto comercial apropriado.
-   Evite criar objetos comerciais que tentem fazer muita coisa. Sobrecarregar objetos comerciais pode significar mais tempo gasto separando o código mais tarde e pode ser uma dor de cabeça de manutenção. Objetos distintos no modelo conceitual não devem ser combinados; Eles devem permanecer com objetos comerciais separados. Você pode lidar com qualquer semelhança usando o código para delegar suas funções comuns a um objeto comercial.
-   Remova todos os objetos comerciais que não forem usados em cenários de uso. Se os objetos se destinam a acomodar o crescimento futuro, considere implementá-los após a conclusão do aplicativo inicial.

Neste ponto, você pode começar a pensar em termos dos computadores e do código. A partir desses serviços corporativos, determine a funcionalidade de exibição e entrada que você precisa fornecer como serviços de usuário. Defina quais tabelas e procedimentos armazenados precisam ser fornecidos como serviços de dados. Para concluir o modelo lógico, defina as interfaces para cada serviço e inclua definições de cada campo de dados e suas regras de validação. Inclua também todas as funções, sua sintaxe e seus parâmetros.

A definição de serviço ou objeto não deve incluir nenhum aspecto da implementação física. A intenção é fornecer uma orientação clara para que os integradores de componentes lógicos trabalhem e para permitir que outros programadores codifiquem partes do aplicativo que possam usar o componente antes que ele seja realmente concluído. No design de modelo lógico, você deve documentar cada tela, função e objeto. Não prossiga para o modelo físico ou a implementação até atender a esses critérios. Se você continuar enquanto o modelo conceitual e o modelo lógico não estiverem no contrato, você terá problemas sérios posteriormente no ciclo de desenvolvimento.

O desenvolvimento incremental de um aplicativo COM+ é comum. Isso envolve criar um subconjunto dos componentes finais e conhecidos e testá-los por meio de cada camada do aplicativo: cliente, negócios e camadas de dados, até o armazenamento de dados. Esse modelo de trabalho fornece informações sobre requisitos adicionais pelo cliente e considerações sobre a implementação. Geralmente, esse modelo de trabalho é testado em um único computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo conceitual: requisitos de aplicativo](the-conceptual-model--application-requirements.md)
</dt> <dt>

[O modelo físico: arquitetura de aplicativo](the-physical-model--application-architecture.md)
</dt> <dt>

[Usando um modelo de arquitetura de Three-Tier](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



