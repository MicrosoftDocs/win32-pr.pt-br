---
title: Inter-Object comunicação
description: O COM foi projetado para permitir que os clientes se comuniquem de forma transparente com objetos, independentemente de onde esses objetos estão sendo executados no mesmo processo, no mesmo computador ou em um computador diferente.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084916"
---
# <a name="inter-object-communication"></a>Inter-Object comunicação

O COM foi projetado para permitir que os clientes se comuniquem de forma transparente com objetos, independentemente de onde esses objetos são runningâs, no mesmo processo, no mesmo computador ou em um computador diferente. Isso fornece um único modelo de programação para todos os tipos de objetos e para clientes de objeto e servidores de objetos.

Do ponto de vista de um cliente, todos os objetos são acessados por meio de ponteiros de interface. Um ponteiro deve estar em processo. Na verdade, qualquer chamada para uma função de interface sempre alcança parte do código em processo primeiro. Se o objeto estiver em processo, a chamada o atingirá diretamente, sem código de infraestrutura de sistema intermediário. Se o objeto estiver fora do processo, a chamada primeiro atingirá o que é chamado de objeto de "proxy" fornecido pelo COM ou pelo objeto (se o implementador quiser). Os pacotes de proxy chamam parâmetros (incluindo qualquer ponteiro de interface) e geram a chamada de procedimento remoto apropriada (ou outro mecanismo de comunicação no caso de proxies gerados personalizados) para o outro processo ou para o outro computador no qual a implementação do objeto está localizada. Esse processo de empacotamento de ponteiros para transmissão entre limites de processo é chamado de *marshaling*.

Do ponto de vista de um servidor, todas as chamadas para as funções de interface de um objeto são feitas por meio de um ponteiro para essa interface. Novamente, um ponteiro tem contexto apenas em um único processo, e o chamador sempre deve ser parte do código em processo. Se o objeto estiver em processo, o chamador será o próprio cliente. Caso contrário, o chamador é um objeto "stub" fornecido pelo COM ou pelo próprio objeto. O stub recebe a chamada de procedimento remoto (ou outro mecanismo de comunicação no caso de proxies gerados personalizados) do "proxy" no processo do cliente, desempacota os parâmetros e chama a interface apropriada no objeto de servidor. A partir dos pontos de vista de clientes e servidores, eles sempre se comunicam diretamente com algum outro código em processo.

O COM fornece uma implementação de marshaling, conhecida como *marshaling padrão*. Essa implementação funciona muito bem para a maioria dos objetos e reduz significativamente os requisitos de programação, tornando o processo de marshaling efetivamente transparente.

No entanto, a separação clara da interface da implementação da transparência do processo do COM pode ser obtida no caminho em algumas situações. O design de uma interface que se concentra em sua função do ponto de vista do cliente pode, às vezes, levar a decisões de design que entram em conflito com a implementação eficiente dessa interface em uma rede. Em casos como esse, o que é necessário não é uma transparência de processo pura, mas "transparência do processo, a menos que você precise se preocupar". COM fornece esse recurso, permitindo que um implementador de objeto dê suporte ao *marshaling personalizado* (também chamado de marshaling [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ). O marshaling padrão é, na verdade, uma instância de marshaling personalizado; é a implementação padrão usada quando um objeto não requer marshaling personalizado.

Você pode implementar o marshaling personalizado para permitir que um objeto execute ações diferentes quando usado por meio de uma rede do que é necessário no acesso local e ele é completamente transparente para o cliente. Essa arquitetura possibilita o design de interfaces de cliente/objeto sem considerar os problemas de desempenho de rede e, posteriormente, resolver problemas de desempenho de rede sem interromper o design estabelecido.

COM não especifica como os componentes são estruturados; Ele especifica como eles interagem. COM deixa a preocupação sobre a estrutura interna de um componente para a programação de linguagens e ambientes de desenvolvimento. Por outro lado, os ambientes de programação não têm padrões definidos para trabalhar com objetos fora do aplicativo imediato. Microsoft Visual C++, por exemplo, funciona muito bem para manipular objetos dentro de um aplicativo, mas não tem suporte para trabalhar com objetos fora do aplicativo. Em geral, todas as outras linguagens de programação são as mesmas nesse aspecto. Portanto, para fornecer interoperabilidade do networkwide, COM, por meio de interfaces independentes de linguagem, o escolhe onde as linguagens de programação deixam.

O indireção duplo da estrutura VTBL significa que os ponteiros na tabela de ponteiros de função não precisam apontar diretamente para a implementação real no objeto real. Esse é o coração da transparência do processo.

Para servidores em processo, em que o objeto é carregado diretamente no processo do cliente, os ponteiros de função na tabela apontam diretamente para a implementação real. Nesse caso, uma chamada de função do cliente para um método de interface transfere diretamente o controle de execução para o método. No entanto, isso não pode funcionar para objetos remotos e autônomos, pois os ponteiros para a memória não podem ser compartilhados entre processos. No entanto, o cliente deve ser capaz de chamar métodos de interface como se estivesse chamando a implementação real. Portanto, o cliente transfere uniformemente o controle para um método em algum objeto fazendo a chamada.

Um cliente sempre chama métodos de interface em algum objeto em processo. Se o objeto real for local ou remoto, a chamada será feita a um objeto proxy, que então faz uma chamada de procedimento remoto para o objeto real.

Então, qual método é realmente executado? A resposta é que sempre que houver uma chamada para uma interface fora do processo, cada método de interface é implementado por um objeto proxy. O objeto proxy sempre é um objeto em processo que age em nome do objeto que está sendo chamado. Esse objeto proxy sabe que o objeto real está sendo executado em um servidor local ou remoto.

O objeto proxy empacota os parâmetros de função em alguns pacotes de dados e gera uma chamada RPC para o objeto local ou remoto. Esse pacote é selecionado por um objeto stub no processo do servidor no local ou em um computador remoto, que desempacota os parâmetros e faz a chamada para a implementação real do método. Quando essa função retorna, o stub empacota todos os parâmetros de saída e o valor de retorno e o envia de volta ao proxy, que os desempacota e os retorna ao cliente original.

Portanto, o cliente e o servidor sempre falam uns com os outros como se tudo estivesse em processo. Todas as chamadas do cliente e todas as chamadas para o servidor são, em algum momento, em processo. Mas como a estrutura VTBL permite que algum agente, como COM, intercepte todas as chamadas de função e todos os retornos de funções, esse agente pode redirecionar essas chamadas para uma chamada RPC, conforme necessário. Embora as chamadas em processo sejam mais rápidas do que as chamadas fora do processo, as diferenças do processo são completamente transparentes para o cliente e o servidor.

Para mais informações, consulte os seguintes tópicos:

-   [Detalhes de marshaling](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Gerenciador](stub.md)
-   [Channel](channel.md)
-   [RPC da Microsoft](microsoft-rpc.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Empacotamento de interface](interface-marshaling.md)
</dt> </dl>

 

 