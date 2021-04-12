---
description: Projetando para implantação
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Projetando para implantação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456956"
---
# <a name="designing-for-deployment"></a>Projetando para implantação

Planejar o escopo de aplicativos COM+ é uma tarefa de design importante que você deve considerar no início. Os sistemas distribuídos que se destinam a serem executados usando COM+ devem ser projetados para implantação com a menor quantidade de configuração individual e para usar com mais eficiência cada processo. Também há técnicas que você pode usar que permitirão obter um desempenho ideal ao implantar um aplicativo COM+. (Para obter mais informações, consulte [implantando para comunicação mais rápida](deploying-for-faster-communication.md).)

Quando exibido com a ferramenta administrativa serviços de componentes, cada aplicativo COM+ aparece como uma pasta dentro da qual os conjuntos de componentes são agrupados logicamente. Embora você possa mover componentes individuais entre pastas de **componentes** de aplicativos do com+ (em outras palavras, de um aplicativo para outro), vários serviços definidos no nível de aplicativo do com+, como segurança, podem ser diferentes. Essas configurações de serviço podem afetar a portabilidade.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Um aplicativo de servidor COM+ define um limite de processo

Ao criar um novo aplicativo de servidor do COM+, você está realmente definindo um novo limite de processo. (Observe a exceção para aplicativos de biblioteca explicados abaixo.) Esse processo torna-se a instância do aplicativo de controle para os componentes contidos no aplicativo COM+. Todos esses componentes são executados em processo em uma nova instância do programa executável COM+ sempre que um programa chama um aplicativo COM+ pela primeira vez. Isso significa que todos os componentes dentro de uma determinada pasta **componentes** do aplicativo com+ são executados em um único espaço de processo que serve como o servidor DCOM. No aplicativo COM+, o COM+ gerencia a memória, coordenação com o Coordenador de Transações Distribuídas (DTC), ativação da instância de componente just-in-time, detecção de falhas e recuperação e segurança baseada em função.

## <a name="calling-across-com-application-boundaries"></a>Chamando entre limites de aplicativos COM+

Como cada aplicativo COM+ normalmente é implementado como um executável separado, o efeito de dividir um aplicativo distribuído em vários aplicativos COM+ apresenta chamadas COM fora do processo quando os componentes em um aplicativo COM+ chamam os componentes em outro aplicativo COM+. Isso apresenta degradação de desempenho devido à sobrecarga extra que o empacotamento de parâmetros COM em processos impõe.

> [!Note]  
> Não há nada inerentemente errado com a incorrência desta penalidade de desempenho; Você só precisa estar ciente de que vai ocorrer. Dependendo do tempo de resposta necessário, o número de usuários que solicitarão serviços de negócios simultaneamente e o ônus de inicialização adicionado que cada componente adiciona a cada aplicativo COM+, você pode descobrir que o impacto no desempenho atribuído a chamadas entre aplicativos é aceitável.

 

Uma possibilidade que elimina a penalidade de desempenho de chamar entre limites de aplicativos COM+ é marcar um determinado aplicativo COM+ como um aplicativo de biblioteca. Um aplicativo de biblioteca COM+ é executado no processo do cliente que o cria. Obviamente, nenhum lucro de desempenho tem nenhum custo. Nesse caso, a compensação envolve as limitações dos aplicativos de biblioteca COM+. Embora um aplicativo de biblioteca possa usar a segurança baseada em função, ele não pode dar suporte a componentes enfileirados ou acesso remoto.

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

 

 



