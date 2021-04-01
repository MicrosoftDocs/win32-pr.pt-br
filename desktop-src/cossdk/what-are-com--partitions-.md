---
description: Uma partição COM+ é um contêiner lógico que permite que os aplicativos sejam executados independentemente de outras configurações desses aplicativos.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: O que são partições COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104091859"
---
# <a name="what-are-com-partitions"></a>O que são partições COM+?

Uma partição COM+ é um contêiner lógico que permite que os aplicativos sejam executados independentemente de outras configurações desses aplicativos. Cada configuração de um aplicativo é instalada em uma partição separada e pode ser gerenciada separadamente, de acordo com as necessidades específicas de seus usuários.

Durante a ativação de um componente COM+, o serviço de partições determina qual configuração do componente será ativada, com base na identidade do usuário que está solicitando a ativação do componente. Por exemplo, uma única organização que tem dois grupos separados, produção e treinamento, pode implementar partições COM+ como uma maneira de permitir que os dois grupos usem configurações diferentes de um aplicativo COM+ no mesmo computador.

**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível. A partição global é a única partição COM+ disponível.

**Windows 2000:** O serviço de partições COM+ não está disponível no Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Benefícios do uso de partições COM+

O uso de partições COM+ oferece várias vantagens, incluindo as seguintes:

-   As organizações podem reduzir o TCO (custo total de propriedade) usando menos servidores de aplicativos físicos para dar suporte a usuários que precisam de várias configurações de aplicativos.
-   A sobrecarga administrativa é reduzida. Em vez de configurar e gerenciar vários computadores, os administradores precisam apenas configurar e gerenciar várias partições no mesmo computador. Além disso, as partições podem ser gerenciadas programaticamente por meio da adição de uma nova interface de programação COM+.
-   A segurança pode ser implementada e gerenciada em uma base partição por partição para usuários locais, usuários de domínio e UOs (unidades organizacionais).
-   Os programadores e administradores podem usar as ferramentas administrativas e de desenvolvimento da Microsoft, como o SDK do Windows, Active Directory usuários e computadores e a ferramenta administrativa serviços de componentes — para gerenciar partições COM+. O recurso de partições é totalmente integrado a essas ferramentas.

## <a name="primary-usage-scenario"></a>Cenário de uso primário

Um dos principais motivos para os clientes implantarem o recurso de partições COM+ é hospedar aplicativos baseados na Web. Por exemplo, suponha que uma pequena empresa de software desenvolve um aplicativo COM+ para uso pelo pessoal do hospital. O aplicativo, que é um aplicativo baseado na Web distribuído, fornece uma maneira para que os hospitais armazenem e recuperem registros médicos de pacientes usando um banco de dados SQL Server.

Suponha que a empresa de software tenha três clientes: hospital A, hospital B e hospital C. Enquanto cada cliente executa o lado do cliente do aplicativo COM+ localmente em seus computadores desktop, o lado do servidor do aplicativo COM+ reside no servidor Web interno da empresa de software e é acessado por seus clientes por meio da Web.

Como cada hospital tem seu próprio conjunto de requisitos de armazenamento e recuperação e seu próprio conjunto de dados de pacientes personalizados, a empresa de software deve fornecer uma maneira para que várias configurações da parte do servidor do aplicativo sejam executadas simultaneamente no servidor Web. As partições COM+ fornecem uma solução para esse problema.

A ilustração a seguir mostra o cenário de partições para o aplicativo COM+ da empresa de software.

![Diagrama que mostra um cenário de partições para um aplicativo COM+, com um aplicativo cliente para o aplicativo de servidor para o banco de dados do SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design de aplicativo](application-design-restrictions.md)
</dt> <dt>

[Componentes e partições em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



