---
title: Lidando com a perda de conectividade
description: Lidando com a perda de conectividade
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eac02c4440cb2e31a29e810d78dfd51764be3ba0ed5a6dc32f8c3e10824bd70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101676"
---
# <a name="dealing-with-loss-of-connectivity"></a>Lidando com a perda de conectividade

Depois que uma chamada RPC é concluída, a conexão não é fechada; Ele é marcado como gratuito. Assim, o servidor pode ficar inativo ou a conectividade de rede pode ser perdida durante ou entre chamadas, enquanto uma conexão está colocada no pool. Como uma questão de política, o tempo de execução de RPC tenta novamente essas chamadas somente se as duas condições a seguir forem atendidas:

-   O servidor não pode possivelmente executar a chamada ou a chamada é idempotente.
-   O cliente pode implementar repetições de maneira eficiente em termos de desempenho.

Os parágrafos a seguir expandem e esclarecem as duas condições.

Uma chamada idempotente é uma chamada que pode ser executada mais de uma vez no servidor sem efeitos colaterais indesejáveis. Por exemplo, ter uma chamada RPC que consulta o saldo no banco de uma determinada conta é idempotente. Se essa chamada for executada duas vezes devido à perda de conectividade, nenhum dano será feito. Outro exemplo de uma chamada idempotente é alterar o endereço de um cliente em um banco de dados. Executar duas vezes é bom, pois a segunda execução simplesmente substitui o endereço já atual pelo mesmo endereço. Uma operação como "subtrair 50 dólares da conta xyz" não é idempotente. A perda de conectividade de rede não deve resultar em várias execuções de tal chamada.

Para ser seguro, o tempo de execução de RPC trata todas as chamadas como não idempotentes. O \[ \] atributo idempotente não tem suporte para [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)e é ignorado. Como tal, a primeira condição na lista anterior é reduzida para *o servidor que não pode executar a chamada*.

Em muitos casos, o tempo de execução de RPC não pode determinar de determinadamente que a chamada ainda não foi executada no servidor. Nesses casos, o cliente não tentará executar a chamada novamente.

Os exemplos a seguir ilustram quando o tempo de execução de RPC faz ou não tenta uma chamada novamente:

-   Um servidor é reinicializado.

    Uma chamada RPC simples, sem segurança, é feita em uma interface na qual nenhuma chamada anterior foi feita após a reinicialização. Como nenhuma chamada foi feita nessa interface, o tempo de execução de RPC primeiro tenta negociar o uso da interface. Ele envia um pacote usando uma conexão no pool. Como o servidor foi reinicializado e a conexão não é mais válida, ela retorna um erro. Como o tempo de execução RPC do lado do cliente ainda não começou a enviar os dados para a chamada real, o cliente determina que o servidor não pôde ter sido executado nesses dados. Portanto, ele fecha a conexão e procura outra conexão no pool. Se não for possível localizar uma conexão, ela abrirá uma nova conexão e tentará negociar o uso da interface novamente. Se isso tiver êxito, a chamada será feita (ou seja, uma nova tentativa será feita, pois a falha foi detectada antes da chamada ser iniciada).

-   Uma chamada RPC com segurança de nível de privacidade (criptografia) é feita em uma conexão com um contexto de segurança já negociado.

    Para garantir um desempenho eficiente, o tempo de execução do RPC criptografa o pacote empacotado embutido (sobre os dados de texto não criptografado). Se a tentativa de enviar os dados falhar, o tempo de execução do RPC não poderá repetir a chamada, já que os dados de texto não criptografado foram substituídos por esses dados e não podem criptografar novamente os dados com um novo contexto de segurança. Portanto, nenhuma repetição é feita.

-   O envio de um fragmento não primeiro falha.

    A repetição não é feita, pois o tempo de execução de RPC pode optar por descartar o conteúdo do primeiro fragmento quando ele for concluído e não tiver como tentar enviar o primeiro fragmento.

-   A solicitação RPC é enviada.

    O servidor anula a conexão. Nenhuma tentativa é feita, já que a RPC não pode distinguir se o servidor recebeu a chamada e começou a executá-la.

Se o servidor usar um ponto de extremidade dinâmico, o RPC não resolverá o ponto de extremidade novamente durante novas tentativas. Isso significa que, se um servidor for desativado e voltar a ficar em funcionamento, ele poderá residir em um ponto de extremidade diferente e o RPC não resolverá de modo transparente o ponto de extremidade quando uma chamada for repetida. Para forçar a reresolução do ponto de extremidade, o cliente RPC deve chamar [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) antes de tentar novamente uma chamada.

Em muitos desses casos, se um cliente RPC puder determinar se uma chamada é idempotente ou se mantém os dados descartados pelo RPC, ele pode optar por criar um mecanismo de repetição sobre o RPC.

> [!Note]  
> Se o servidor for um cluster e os diferentes nós do cluster executarem versões diferentes do software do servidor, uma nova tentativa de RPC poderá chamar a chamada em um nó diferente do cluster no caso de failover e, potencialmente, em uma versão diferente do servidor. Nesses cenários de implantação, verifique se o cliente não depende de uma versão específica do software de servidor para executar uma determinada chamada. Se tiver, o cliente deverá criar um mecanismo sobre o RPC que detecta e manipula essas condições.

 

 

 