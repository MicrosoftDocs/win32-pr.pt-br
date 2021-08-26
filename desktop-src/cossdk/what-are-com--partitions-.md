---
description: Uma partição COM+ é um contêiner lógico que permite que os aplicativos executem independentemente de outras configurações desses aplicativos.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: O que são partições COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc678089948770181d98af065afa414741055062ed2e942215de5d7cb8bc7b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070256"
---
# <a name="what-are-com-partitions"></a>O que são partições COM+?

Uma partição COM+ é um contêiner lógico que permite que os aplicativos executem independentemente de outras configurações desses aplicativos. Cada configuração de um aplicativo é instalada em uma partição separada e pode ser gerenciada separadamente, de acordo com as necessidades específicas de seus usuários.

Durante a ativação de um componente COM+, o serviço de partições determina qual configuração do componente deve ser ativada, com base na identidade do usuário que está solicitando a ativação do componente. Por exemplo, uma única organização que tem dois grupos separados, Produção e Treinamento, pode implementar partições COM+ como uma maneira de permitir que os dois grupos usem configurações diferentes de um aplicativo COM+ no mesmo computador.

**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível. A partição global é a única partição COM+ disponível.

**Windows 2000:** O serviço de partições COM+ não está disponível no Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Benefícios do uso de partições COM+

O uso de partições COM+ oferece várias vantagens, incluindo as seguintes:

-   As organizações podem reduzir seu TCO (custo total de propriedade) usando menos servidores de aplicativos físicos para dar suporte a usuários que precisam de várias configurações de aplicativo.
-   A sobrecarga administrativa é reduzida. Em vez de precisar configurar e gerenciar vários computadores, os administradores só precisam configurar e gerenciar várias partições no mesmo computador. Além disso, as partições podem ser gerenciadas programaticamente por meio da adição de uma nova interface de programação COM+.
-   A segurança pode ser implementada e gerenciada particionada por partição para usuários locais, usuários de domínio e unidades organizacionais (OUs).
-   Os programadores e administradores podem usar as ferramentas administrativas e de desenvolvimento da Microsoft, como o SDK do Windows, Usuários e Computadores do Active Directory e a ferramenta administrativa dos Serviços de Componentes, para gerenciar partições COM+. O recurso de partições é totalmente integrado a essas ferramentas.

## <a name="primary-usage-scenario"></a>Cenário de uso primário

Um principal motivo para os clientes implantarem o recurso de partições COM+ é hospedar aplicativos baseados na Web. Por exemplo, suponha que uma pequena empresa de software desenvolva um aplicativo COM+ para uso pela equipe do hospital. O aplicativo, que é um aplicativo distribuído baseado na Web, fornece uma maneira para os médicos armazenarem e recuperarem registros médicos de pacientes usando um banco de dados SQL Server de saúde.

Suponha que a empresa de software tenha três clientes: Hospital A, Hospital B e Hospital C. Embora cada cliente executa o lado do cliente do aplicativo COM+ localmente em seus computadores desktop, o lado do servidor do aplicativo COM+ reside no servidor Web interna da empresa de software e é acessado por seus clientes por meio da Web.

Como cada hospital tem seu próprio conjunto de requisitos de armazenamento e recuperação e seu próprio conjunto de dados de pacientes personalizados, a empresa de software deve fornecer uma maneira para que várias configurações da parte do servidor do aplicativo sejam executadas simultaneamente no servidor Web. As partições COM+ fornecem uma solução para esse problema.

A ilustração a seguir mostra o cenário de partições para o aplicativo COM+ da empresa de software.

![Diagrama que mostra um cenário de partições para um aplicativo COM+, com um aplicativo cliente para aplicativo de servidor para o banco de dados SQL servidor.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design do aplicativo](application-design-restrictions.md)
</dt> <dt>

[Partições e componentes em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



