---
title: Alterando interfaces de maneira compatível com versões anteriores
description: Os métodos explicados em The Versioning Theory para RPC e COM podem ser inaceitáveis por muitos motivos.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbe06be3106b4c599baed2d625eefa1f9c7d035c70ef89ac325406bb8c2037d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022956"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Alterando interfaces de maneira compatível com versões anteriores

Os métodos explicados em [The Versioning Theory para RPC e COM](the-versioning-theory-for-rpc-and-com.md) podem ser inaceitáveis por muitos motivos. Alterar uma versão de interface de acordo com as regras exige essencialmente que novos clientes não se comuniquem com servidores antigos. Isso geralmente é impossível com o software comercial implantado no campo. Às vezes, Windows introduziu alterações de interface ausentes de GUIDs ou versões alteradas. Isso foi resultado da necessidade de novos clientes se comunicarem com servidores herdados e porque a solução que um novo cliente poderia dar suporte às interfaces antiga e nova era considerada indesejável.

## <a name="best-practice"></a>Melhor prática

Esses são os métodos razoáveis de trabalhar em torno do problema de incompatibilidade de transmissão quando o GUID e a versão da interface não podem ser alterados.

1.  Que o aplicativo esteja ciente das funcionalidades do outro lado.

    O cliente e o servidor têm um protocolo que permite que cada (ou pelo menos o novo cliente) estabeleça a identidade do parceiro. Normalmente, é suficiente que o novo cliente esteja ciente dos recursos com suporte em servidores novos e antigos. Isso pode ser feito facilmente quando um aplicativo mantém um contexto de conexão e tem suporte por meio de um tipo *XxxGetInfo* de chamada de função executada pelo cliente antes de executar qualquer operação RPC. Quando um aplicativo gerencia os recursos por servidor, uma chamada com uma incompatibilidade com o servidor/cliente antigo nunca pode ocorrer, pois o aplicativo controla quais chamadas são emitidas para qual servidor. A parte inferior é que o aplicativo é proativo para impedir que ocorra uma incompatibilidade. Isso pode ser executado em conjunto com a segunda prática.

2.  Introduzir uma nova API remota.

    Um novo método remoto não colide com métodos existentes se ele for adicionado no final da interface. Clientes antigos podem chamar novos servidores como sempre. O novo cliente pode chamar o novo método sem saber a identidade do servidor, desde que ele veja os erros provenientes do servidor que está sendo chamado. O tempo de executar RPC sempre verifica o número do método para cada interface antes de uma expedição para garantir que o método está dentro de uma tabela v apropriada. Para um método desconhecido para um servidor, o tempo de executar RPC gera a exceção RPC \_ S \_ PROCNUM \_ OUT OF \_ \_ RANGE. Essa exceção é criada somente nessa situação específica. Portanto, um novo cliente pode observar a exceção como um sinal de que a chamada foi para um servidor antigo e pode modificar seu comportamento normalmente.

3.  Introduza novos parâmetros ou novos tipos de dados somente nos novos métodos.

    Um motivo para introduzir um novo método é evitar a incompatibilidade de dados. Se um novo tipo de dados for introduzido ou simplesmente modificado, em princípio, ele deverá ser usado somente em um novo método (ou métodos). Consulte [Exemplos de alterações incompatíveis para](examples-of-incompatible-changes.md) ver exemplos de alterações de tipo de dados incompatíveis. A única exceção notável para essa regra é descrita no item quatro.

4.  Mapeie novos parâmetros ou novos tipos de dados por meio de um wrapper.

    Essa solução se aplica quando um novo parâmetro ou tipo de dados deve ser exposto a um usuário, mas, na verdade, não precisa ser remoto separadamente ou pode ser mapeado para os tipos de dados ou parâmetros antigos. Por exemplo, muitas APIs do sistema são voltas e executam uma chamada remota. Eles podem ou não estar fazendo algum tipo de mapeamento dos tipos de dados conhecidos pelo usuário para os tipos de dados realmente usados na chamada RPC subjacente. Portanto, sempre vale a pena examinar se a alteração na interface do usuário precisa ser propagada como uma alteração em uma interface remota.

    Uma situação semelhante pode ocorrer quando o usuário chama uma API remota diretamente, mas um wrapper pode ser introduzido para fazer um novo mapeamento de tipo ou algumas outras ações adicionais que se tornaram necessárias. A IDL (Linguagem de Definição de Interface) tem várias maneiras de facilitar o remapeamento, ou seja, chamar como , transmitir \[ [**\_**](/windows/desktop/Midl/call-as) \] \[ [**\_ como**](/windows/desktop/Midl/transmit-as) \] e efetuar \[ [**\_ marshaling de transmissão.**](/windows/desktop/Midl/wire-marshal) \] A \[ **chamada \_ como** \] atributo introduz um wrapper de função no cliente e no servidor. Ambos são colocados entre o código do usuário e o marshaler. Os outros atributos lidam com o mapeamento de tipo direto. Para problemas de extensão, chame como é usado com mais frequência e é mais fácil de entender e manipular sem \[ **\_** \] armadilhas.

5.  Modificar tipos de dados por meio de uma união sem padrão.

    A alteração de um atributo ou tipo de dados normalmente leva à incompatibilidade de transmissão. Consulte [Exemplos de alterações incompatíveis](examples-of-incompatible-changes.md) para ver exemplos. No entanto, no caso de uma união sem uma cláusula padrão, a incompatibilidade pode ser gerenciada de maneira semelhante ao caso de um procedimento fora do intervalo, conforme descrito anteriormente. Esse esquema é prontamente aplicável aos populares *tipos XxxINFO* que usam uniões.

    Por exemplo, uma chamada como esta

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    poderia retornar informações no nível 1, 2 ou 3, com *XxxINFO* sendo uma união com três branches: 1, 2 e 3.

6.  Use o \[ [**atributo range**](/windows/desktop/Midl/range) \] para especificar o intervalo.

    Você pode especificar o atributo \[ [**de intervalo**](/windows/desktop/Midl/range) \] em um tipo de escala simples sem quebrar a compatibilidade com compatibilidade com compatibilidade com compatibilidade com rót. Esse atributo não afeta o formato de transmissão, mas durante a unmarshalling RPC verifica o valor na transmissão para confirmar que ele está dentro do intervalo especificado no arquivo .idl. Caso não seja, uma exceção RPC \_ X INVALID BOUND será \_ \_ lançada. Isso será especialmente útil se o servidor souber o tamanho máximo de uma matriz dimensionada.

    Por exemplo:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

O comportamento de RPC quando o nível indicado é 4 e o arm está ausente, depende da definição da união. Para uma união com a cláusula padrão definida, o RPC transmite um tipo indicado na cláusula padrão para qualquer coisa diferente dos rótulos de arm conhecidos (nesse caso, qualquer coisa diferente de 1, 2 ou 3). Para uma união sem padrão, o unmarshaler gera uma exceção porque, por definição, não há padrão para o fall back. A exceção é RPC \_ S \_ INVALID \_ TAG.

Novamente, um novo cliente pode ajustar seu comportamento ao descobrir que ele chamou um servidor antigo.

O que segue estas práticas recomendadas é que, se um tipo de dados remotamente remota deve ser projetado que pode ser estendido no futuro, use uma união sem padrão no arquivo IDL. Dada uma escolha, uma união encapsulada é um pouco mais limpa.

Devido a problemas de representação interna do protocolo de transmissão NDR64, a recomendação para adicionar os braços fornecidos anteriormente nesta seção precisa ser qualificada da seguinte maneira: o novo braço que está sendo adicionado não pode alterar o alinhamento da união e, em particular, o maior alinhamento dos braços não deve mudar. Normalmente, isso não é um problema, pois um ponteiro em um arm força o alinhamento a 8. Um design em que cada arm é um ponteiro para um tipo de arm é uma maneira limpa de atender ao requisito.

 

 