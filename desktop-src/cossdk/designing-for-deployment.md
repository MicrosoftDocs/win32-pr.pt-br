---
description: Projetando para implantação
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Projetando para implantação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a755132f1be35ecb6913b7690bce11e342fceb957e63607ee4e9b579bcc758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307293"
---
# <a name="designing-for-deployment"></a>Projetando para implantação

Planejar o escopo de aplicativos COM+ é uma tarefa de design importante que você deve considerar no início. Os sistemas distribuídos destinados a serem executados usando COM+ devem ser projetados para implantação com a menor quantidade de configuração individual e para usar cada processo com mais eficiência. Também há técnicas que você pode usar que permitirão que você alcance o desempenho ideal ao implantar um aplicativo COM+. (Para obter mais informações, consulte [Implantando para comunicação mais rápida](deploying-for-faster-communication.md).)

Quando exibido com a ferramenta administrativa Serviços de Componentes, cada aplicativo COM+ aparece como uma pasta na qual os conjuntos de componentes são agrupados logicamente. Embora você possa mover componentes  individuais entre pastas componentes do aplicativo COM+ (em outras palavras, de um aplicativo para outro), vários serviços definidos no nível do aplicativo COM+, como segurança, podem ser diferentes. Essas configurações de serviço podem afetar a portabilidade.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Um aplicativo de servidor COM+ define um limite de processo

Ao criar um novo aplicativo de servidor COM+, você está realmente definindo um novo limite de processo. (Observe a exceção para aplicativos de biblioteca explicados abaixo.) Esse processo se torna a instância de aplicativo de controle para os componentes contidos no aplicativo COM+. Todos esses componentes são executados em processo em uma nova instância do programa executável COM+ sempre que um programa chama um aplicativo COM+ pela primeira vez. Isso significa que todos os componentes dentro  da pasta Componentes de um determinado aplicativo COM+ são executados em um único espaço de processo que serve como o servidor DCOM. No aplicativo COM+, o COM+ gerencia a memória, a coordenação com o DTC (Coordenador de Transações Distribuídas), a ativação de instância de componente Just-In-Time, a detecção e a recuperação de falhas e a segurança baseada em função.

## <a name="calling-across-com-application-boundaries"></a>Chamando entre limites de aplicativo COM+

Como cada aplicativo COM+ normalmente é implementado como um executável separado, o efeito de dividir um aplicativo distribuído entre vários aplicativos COM+ introduz chamadas COM fora do processo quando componentes em um aplicativo COM+ chamam os componentes em outro aplicativo COM+. Isso introduz a degradação do desempenho devido à carga extra que o marshaling de parâmetros COM em processos impõe.

> [!Note]  
> Não há nada inerentemente errado em incorrer nessa penalidade de desempenho; você só precisa estar ciente de que isso ocorrerá. Dependendo do tempo de resposta necessário, do número de usuários que solicitarão simultaneamente serviços de negócios e da carga de início adicionada que cada componente adiciona a cada aplicativo COM+, você poderá descobrir que o desempenho atribuível a chamadas entre aplicativos é aceitável.

 

Uma possibilidade que elimina a penalidade de desempenho de chamar entre limites de aplicativo COM+ é marcar um determinado aplicativo COM+ como um aplicativo de biblioteca. Um aplicativo de biblioteca COM+ é executado no processo do cliente que o cria. É claro que nenhum ganho de desempenho tem custo zero. Nesse caso, a troca envolve as limitações de aplicativos de biblioteca COM+. Embora um aplicativo de biblioteca possa usar a segurança baseada em função, ele não pode dar suporte a componentes em fila ou acesso remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implantando para comunicação mais rápida](deploying-for-faster-communication.md)
</dt> <dt>

[Projetando para disponibilidade](designing-for-availability.md)
</dt> <dt>

[Projetando para escalabilidade](designing-for-scalability.md)
</dt> <dt>

[Projetando para segurança](designing-for-security.md)
</dt> </dl>

 

 



