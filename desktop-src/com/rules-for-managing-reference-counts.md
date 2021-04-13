---
title: Regras para gerenciar contagens de referência
description: Usar uma contagem de referência para gerenciar o tempo de vida de um objeto permite que vários clientes obtenham e liberem o acesso a um único objeto sem precisar coordenar um ao outro no gerenciamento do tempo de vida do objeto.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366743"
---
# <a name="rules-for-managing-reference-counts"></a>Regras para gerenciar contagens de referência

Usar uma contagem de referência para gerenciar o tempo de vida de um objeto permite que vários clientes obtenham e liberem o acesso a um único objeto sem precisar coordenar um ao outro no gerenciamento do tempo de vida do objeto. Desde que o objeto cliente esteja em conformidade com determinadas regras de uso, o objeto, em vigor, fornece esse gerenciamento. Essas regras especificam como gerenciar referências entre objetos. (COM não especifica implementações internas de objetos, embora essas regras sejam um ponto de partida razoável para uma política dentro de um objeto.)

Conceitualmente, os ponteiros de interface podem ser considerados como residentes em variáveis de ponteiro que incluem todo o estado de computação interno que mantém um ponteiro de interface. Isso incluiria variáveis em locais de memória, em registros de processador internos e em ambas as variáveis geradas pelo programador e por compilador. A atribuição ou a inicialização de uma variável de ponteiro envolve a criação de uma nova cópia de um ponteiro já existente. Quando houve uma cópia do ponteiro em alguma variável (o valor usado na atribuição/inicialização), agora há duas. Uma atribuição a uma variável de ponteiro destrói a cópia do ponteiro no momento na variável, assim como faz a destruição da própria variável. (Ou seja, o escopo no qual a variável é encontrada, como o quadro de pilha, é destruído.)

Da perspectiva de um cliente COM, a contagem de referência é sempre feita para cada interface. Os clientes nunca devem supor que um objeto usa o mesmo contador para todas as interfaces.

O caso padrão é que [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve ser chamado para cada nova cópia de um ponteiro de interface e [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) deve ser chamada para cada destruição de um ponteiro de interface, exceto quando as seguintes regras permitirem o contrário:

-   **Parâmetros de entrada para o functions.** O chamador deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) no parâmetro porque ele será liberado (com uma chamada para [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) no código de implementação quando o valor out for armazenado sobre ele.
-   **Buscando uma variável global.** Ao criar uma cópia local de um ponteiro de interface de uma cópia existente do ponteiro em uma variável global, você deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na cópia local porque outra função pode destruir a cópia na variável global enquanto a cópia local ainda é válida.
-   **Novos ponteiros sintetizados fora de "ar fino".** Uma função que sintetiza um ponteiro de interface usando conhecimento interno especial em vez de obtê-lo de alguma outra fonte deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) inicialmente no ponteiro recentemente sintetizado. Exemplos importantes dessas rotinas incluem rotinas de criação de instância, implementações de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))e assim por diante.
-   **Recuperando uma cópia de um ponteiro armazenado internamente.** Quando uma função recupera uma cópia de um ponteiro armazenado internamente pelo objeto chamado, o código desse objeto deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) no ponteiro antes que a função retorne. Depois que o ponteiro for recuperado, o objeto de origem não terá nenhuma outra maneira de determinar como seu tempo de vida se relaciona com o da cópia armazenada internamente do ponteiro.

As únicas exceções ao caso padrão exigem que o código de gerenciamento Conheça as relações dos tempos de vida de duas ou mais cópias de um ponteiro para a mesma interface em um objeto e simplesmente certifique-se de que o objeto não seja destruído, permitindo que sua contagem de referência vá para zero. Em geral, há dois casos, da seguinte maneira:

-   Quando uma cópia de um ponteiro já existe e um segundo é criado posteriormente e, em seguida, é destruído enquanto a primeira cópia ainda existe, as chamadas para [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)para a segunda cópia podem ser omitidas.
-   Quando existe uma cópia de um ponteiro e um segundo é criado e o primeiro é destruído antes do segundo, as chamadas para [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)para a segunda cópia e para [**liberação**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) da primeira cópia podem ser omitidas.

Veja a seguir exemplos específicos dessas situações, as duas primeiras são especialmente comuns:

-   **Em parâmetros para funções.** O tempo de vida da cópia de um ponteiro de interface passado como um parâmetro para uma função é aninhado no ponteiro usado para inicializar o valor, portanto, não há necessidade de uma contagem de referência separada no parâmetro.
-   **Parâmetros de saída das funções, incluindo valores de retorno.** Para definir o parâmetro out, a função deve ter uma cópia estável do ponteiro de interface. No retorno, o chamador é responsável por liberar o ponteiro. Portanto, o parâmetro out não precisa de uma contagem de referência separada.
-   **Variáveis locais.** Uma implementação de método tem controle dos tempos de vida de cada uma das variáveis de ponteiro alocadas no quadro de pilha e pode usá-la para determinar como omitir pares de liberação [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)redundantes / [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .
-   **Pontos de extremidade.** Algumas estruturas de dados contêm dois objetos, cada um com um ponteiro para o outro. Se o tempo de vida do primeiro objeto for conhecido por conter o tempo de vida do segundo, não será necessário ter uma contagem de referência no ponteiro do segundo objeto para o primeiro objeto. Muitas vezes, evitar esse ciclo é importante para manter o comportamento de desalocação apropriado. No entanto, os ponteiros sem desconto devem ser usados com extrema cautela, pois a parte do sistema operacional que lida com o processamento remoto não tem como saber mais sobre essa relação. Portanto, em quase todos os casos, ter o ponto de extremidade vê um segundo, o objeto "Friend" do primeiro ponteiro (evitando, portanto, a circularidade) é a solução preferida. A arquitetura de objetos conectáveis do COM, por exemplo, usa essa abordagem.

Ao implementar ou usar objetos de referência contados, pode ser útil aplicar *contagens de referência artificial*, que garantem a estabilidade do objeto durante o processamento de uma função. Ao implementar um método de uma interface, você pode chamar funções que têm a chance de decrementar sua contagem de referência para um objeto, causando uma liberação prematura do objeto e a falha da implementação. Uma maneira robusta de evitar isso é inserir uma chamada para [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) no início da implementação do método e emparelhar isso com uma chamada para [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) logo antes do retorno do método.

Em algumas situações, os valores de retorno de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) podem ser instáveis e não devem ser dependentes; Eles devem ser usados somente para fins de depuração ou diagnóstico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando tempos de vida de objeto por meio de contagem de referência](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 