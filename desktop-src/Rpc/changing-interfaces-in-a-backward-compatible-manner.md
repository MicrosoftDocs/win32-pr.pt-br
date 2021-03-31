---
title: Alterando interfaces de maneira compatível com versões anteriores
description: Os métodos explicados na teoria do controle de versão para RPC e COM podem ser inaceitáveis por vários motivos.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314daecc6b55aaf4a348411010eb578149f86921
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641725"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Alterando interfaces de maneira compatível com versões anteriores

Os métodos explicados na [teoria do controle de versão para RPC e com](the-versioning-theory-for-rpc-and-com.md) podem ser inaceitáveis por vários motivos. A alteração de uma versão de interface de acordo com as regras requer basicamente que novos clientes não se comuniquem com servidores antigos. Isso geralmente é impossível com software comercial implantado no campo. Às vezes, o Windows introduziu alterações de interface ausentes de GUIDs ou versões alteradas. Isso foi resultado de novos clientes que precisam se comunicar com servidores herdados e porque a solução que um novo cliente ofereceria às interfaces antiga e nova foi considerada indesejável.

## <a name="best-practice"></a>Melhor prática

Esses são os métodos razoáveis de trabalhar em relação ao problema de incompatibilidade de conexão quando o GUID e a versão da interface não podem ser alterados.

1.  Faça com que o aplicativo esteja ciente dos recursos do outro lado.

    O cliente e o servidor têm um protocolo que permite que cada um (ou pelo menos o novo cliente) estabeleça a identidade do parceiro. Normalmente, é suficiente que o novo cliente esteja ciente dos recursos com suporte dos servidores novos e antigos. Isso pode ser feito facilmente quando um aplicativo mantém em um contexto de conexão e tem suporte por meio de um tipo *XxxGetInfo* de chamada de função executado pelo cliente antes de executar qualquer operação RPC. Quando um aplicativo gerencia os recursos em uma base de versão por servidor, uma chamada com uma incompatibilidade para o servidor/cliente antigo nunca pode ocorrer, já que o aplicativo controla quais chamadas são emitidas para qual servidor. O resultado final é que o aplicativo é proativo para impedir que uma incompatibilidade ocorra. Isso pode ser realizado em conjunto com a segunda prática.

2.  Introduza uma nova API remota.

    Um novo método remoto não colidirá com os métodos existentes se ele for adicionado no final da interface. Clientes antigos podem chamar novos servidores como sempre têm. O novo cliente pode chamar o novo método sem saber a identidade do servidor, desde que ele Observe os erros provenientes do servidor que está sendo chamado. O tempo de execução RPC sempre verifica o número do método para cada interface antes de uma expedição para garantir que o método esteja dentro de uma tabela v apropriada. Para um método que é desconhecido para um servidor, o tempo de execução de RPC gera a exceção RPC \_ S \_ PROCNUM \_ fora \_ do \_ intervalo. Essa exceção é gerada somente nesta situação específica. Portanto, um novo cliente pode observar a exceção como um sinal de que a chamada foi enviada para um servidor antigo e pode modificar seu comportamento normalmente.

3.  Introduza novos parâmetros ou novos tipos de dados apenas nos novos métodos.

    Um motivo para introduzir um novo método é evitar a incompatibilidade de dados. Se um novo tipo de dados for introduzido ou simplesmente modificado, em princípio, ele deve ser usado somente em um novo método (ou métodos). Veja [exemplos de alterações incompatíveis](examples-of-incompatible-changes.md) para obter exemplos de alterações de tipo de dados incompatíveis. A única exceção notável a essa regra é descrita no item quatro.

4.  Mapeie novos parâmetros ou novos tipos de dados por meio de um wrapper.

    Essa solução se aplica quando um novo parâmetro ou tipo de dados deve ser exposto a um usuário, mas, na verdade, não precisa ser remoto separadamente ou pode ser mapeado para os tipos de dados ou parâmetros antigos. Por exemplo, muitas APIs de sistema desenvolvem e executam uma chamada remota. Eles podem ou não estar fazendo algum tipo de mapeamento dos tipos de dados conhecidos do usuário para os tipos de dados realmente usados na chamada RPC subjacente. Portanto, vale a pena examinar se a alteração na interface do usuário precisa ser propagada como uma alteração para uma interface remota.

    Uma situação semelhante pode ocorrer quando o usuário chama uma API remota diretamente, mas um wrapper pode ser introduzido para fazer um novo mapeamento de tipo ou outras ações adicionais que se tornaram necessárias. A IDL (Interface Definition Language) tem várias maneiras de facilitar esse remapeamento, como \[ [**chamar \_ como**](/windows/desktop/Midl/call-as) \] , \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] e \[ [**\_ realizar marshaling**](/windows/desktop/Midl/wire-marshal) \] . O \[ atributo **Call \_ as** \] introduz um wrapper de função no cliente e no servidor. Ambos são colocados entre o código do usuário e o marshaler. Os outros atributos lidam com o mapeamento de tipo direto. Para problemas de extensão, \[ **chame \_ como** \] é o usado com mais frequência e é mais fácil de entender e manipular sem armadilhas.

5.  Modifique os tipos de dados por meio de uma União defaultless.

    A alteração de um atributo ou tipo de dados geralmente leva a uma incompatibilidade. Consulte [exemplos de alterações incompatíveis](examples-of-incompatible-changes.md) para obter exemplos. No entanto, no caso de uma União sem uma cláusula padrão, a incompatibilidade pode ser gerenciada de forma semelhante ao caso de um procedimento fora do intervalo, conforme descrito anteriormente. Esse esquema é prontamente aplicável aos tipos populares de *XxxINFO* que usam uniões.

    Por exemplo, uma chamada como esta

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    pode retornar informações no nível 1, 2 ou 3, com *XxxINFO* sendo uma União com três ramificações: 1, 2 e 3.

6.  Use o \[ atributo [**Range**](/windows/desktop/Midl/range) \] para especificar o intervalo.

    Você pode especificar o \[ atributo de [**intervalo**](/windows/desktop/Midl/range) \] em um tipo de escala simples sem interromper a compatibilidade com versões anteriores. Esse atributo não afeta o formato de conexão, mas durante o desempacotamento RPC verifica o valor em fio para confirmar que ele está dentro do intervalo especificado no arquivo. idl. Caso contrário, uma exceção de associação de RPC \_ X \_ inválida \_ será lançada. Isso é especialmente útil se o servidor souber o tamanho máximo de uma matriz dimensionada.

    Por exemplo:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

O comportamento de RPC quando o nível indicado é 4 e o ARM está ausente, depende da definição da União. Para uma União com a cláusula default definida, o RPC transmite um tipo indicado na cláusula default para qualquer coisa diferente dos rótulos de ARM conhecidos (nesse caso, algo diferente de 1, 2 ou 3). Para uma União defaultmenos, o desempacotador gera uma exceção porque, por definição, não há nenhum padrão para fazer fallback. A exceção é uma \_ marca de RPC S \_ inválida \_ .

Novamente, um novo cliente pode ajustar seu comportamento na descoberta de que ele chamou um servidor antigo.

O que vem a seguir dessas práticas recomendadas é que, se um tipo de dados remoto tiver de ser criado, isso poderá ser estendido no futuro, use uma União defaultless no arquivo IDL. Dada uma escolha, uma União encapsulada é um pouco mais limpa.

Devido a peculiaridades da representação interna do protocolo de fio NDR64, a recomendação para adicionar braços fornecidos anteriormente nesta seção precisa ser qualificada da seguinte maneira: o novo ARM que está sendo adicionado não pode alterar o alinhamento da União e, em particular, o maior alinhamento dos braços não deve ser alterado. Isso normalmente não é um problema, uma vez que um ponteiro em um ARM força o alinhamento a 8. Um design em que cada ARM é um ponteiro para um tipo de ARM é uma maneira limpa de satisfazer o requisito.

 

 