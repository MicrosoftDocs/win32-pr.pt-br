---
title: Registrando interfaces
description: Registrando uma interface RPC (chamada de procedimento remoto).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159289"
---
# <a name="registering-interfaces"></a>Registrando interfaces

Esta seção apresenta uma discussão detalhada sobre o processo de registro de uma interface RPC.

As informações nesta seção são apresentadas nos seguintes tópicos:

-   [Funções de registro de interface](#interface-registration-functions)
-   [Vetores de ponto de entrada](#entry-point-vectors)
-   [EPVs Manager](#manager-epvs)
-   [Registrando uma única implementação de uma interface](#registering-a-single-implementation-of-an-interface)
-   [Registrando várias implementações de uma interface](#registering-multiple-implementations-of-an-interface)
-   [Regras para invocar rotinas do Gerenciador](#rules-for-invoking-manager-routines)
-   [Expedindo uma chamada de procedimento remoto para uma rotina de Server-Manager](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Fornecendo sua própria função Object-Inquiry](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Funções de registro de interface

Os servidores registram suas interfaces chamando a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) . Os programas de servidor complexos geralmente dão suporte a mais de uma interface. Os aplicativos de servidor devem chamar essa função uma vez para cada interface com suporte.

Além disso, os servidores podem dar suporte a várias versões da mesma interface, cada uma com sua própria implementação das funções da interface. Se o seu programa de servidor faz isso, ele deve fornecer um conjunto de pontos de entrada. Um ponto de entrada é uma rotina de gerente que despacha chamadas para uma versão de uma interface. Deve haver um ponto de entrada para cada versão da interface. O grupo de pontos de entrada é chamado de vetor de ponto de entrada. Para obter detalhes, consulte [vetores de ponto de entrada](#entry-point-vectors).

Além da função padrão [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), o RPC também oferece suporte a outras funções de registro de interface. A função [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) estende os recursos do **RpcServerRegisterIf** permitindo que você especifique um conjunto de sinalizadores de registro (consulte [sinalizadores de registro de interface](interface-registration-flags.md)), o número máximo de solicitações simultâneas de chamada de procedimento remoto que o servidor pode aceitar e o tamanho máximo em bytes de blocos de dados de entrada.

A Biblioteca RPC também contém uma função chamada [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex). Assim como a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , essa função registra uma interface. O programa de servidor também pode usar essa função para especificar um conjunto de sinalizadores de registro (consulte [sinalizadores de registro de interface](interface-registration-flags.md)), o número máximo de solicitações simultâneas de chamada de procedimento remoto que o servidor pode aceitar e uma função de retorno de chamada de segurança.

As funções [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)e [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) definem valores na tabela interna do registro de interface. Esta tabela é usada para mapear o UUID de interface e UUIDs de objeto para um EPV de gerente. O Gerenciador EPV é uma matriz de ponteiros de função que contém exatamente um ponteiro de função para cada protótipo de função na interface especificada no arquivo IDL.

Para obter informações sobre como fornecer vários EPVs para fornecer várias implementações da interface, consulte [várias implementações de interface](#registering-multiple-implementations-of-an-interface).

A biblioteca de tempo de execução usa a tabela de registro de interface (definida por chamadas para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) e a tabela de registro de objeto (definida por chamadas para a função [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) para mapear a interface e os UUIDs de objeto para o ponteiro de função.

Quando desejar que o seu programa de servidor remova uma interface do registro de biblioteca de tempo de execução RPC, chame a função [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) . Depois que a interface for removida do registro, a biblioteca de tempo de execução RPC não aceitará mais novas chamadas para essa interface.

## <a name="entry-point-vectors"></a>Vetores de ponto de entrada

O vetor de ponto de entrada do Gerenciador (EPV) é uma matriz de ponteiros de função que aponta para implementações das funções especificadas no arquivo IDL. O número de elementos na matriz corresponde ao número de funções especificadas no arquivo IDL. O RPC dá suporte a vários vetores de ponto de entrada que representam várias implementações das funções especificadas na interface.

O compilador MIDL gera automaticamente um tipo de dados EPV Manager para uso na construção do EPVs do Gerenciador. O tipo de dados é denominado * If-name ***\_ Server \_ EPV**, em que *If-name* especifica o identificador de interface no arquivo IDL.

O compilador MIDL cria e inicializa automaticamente um gerenciador padrão EPV na suposição de que existe uma rotina de gerente de mesmo nome para cada procedimento na interface e é especificada no arquivo IDL.

Quando um servidor oferece várias implementações da mesma interface, o servidor deve criar um EPV do Gerenciador adicional para cada implementação. Cada EPV deve conter exatamente um ponto de entrada (endereço de uma função) para cada procedimento definido no arquivo IDL. O aplicativo de servidor declara e Inicializa uma variável EPV de Gerenciador do tipo *If-name * * * \_ Server \_ EPV** para cada implementação adicional da interface. Para registrar o EPVs, ele chama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) uma vez para cada tipo de objeto ao qual ele dá suporte.

Quando o cliente faz uma chamada de procedimento remoto para o servidor, o EPV que contém o ponteiro de função é selecionado com base no UUID da interface e no tipo de objeto. O tipo de objeto é derivado do UUID de objeto pela função Object-inquire ou o mapeamento controlado por tabela controlado por [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).

## <a name="manager-epvs"></a>EPVs Manager

Por padrão, o compilador MIDL usa os nomes de procedimento do arquivo IDL de uma interface para gerar um EPV de gerente, que o compilador coloca diretamente no stub do servidor. Esse EPV padrão é inicializado estaticamente usando os nomes de procedimento declarados na definição de interface.

Para registrar um gerente usando o EPV padrão, especifique **NULL** como o valor do parâmetro *MgrEpv* em uma chamada para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) . Se os nomes de rotina usados por um gerente corresponderem aos da definição da interface, você poderá registrar esse Gerenciador usando o EPV padrão da interface gerada pelo compilador MIDL. Você também pode registrar um gerente usando um EPV que o aplicativo de servidor fornece.

Um servidor pode (e às vezes deve) criar e registrar um EPV de Gerenciador não **nulo** para uma interface. Para selecionar um aplicativo de servidor – fornecido EPV, passe o endereço de um EPV cujo valor foi declarado pelo servidor como o valor do *MgrEpv* um parâmetro. Um valor não **nulo** para o *MgrEpv* um parâmetro sempre substitui um EPV padrão no stub do servidor.

O compilador MIDL gera automaticamente um tipo de dados EPV Manager (RPC \_ Mgr \_ EPV) para um aplicativo de servidor usar no EPVs do Gerenciador de construção. Um EPV de gerente deve conter exatamente um ponto de entrada (endereço de função) para cada procedimento definido no arquivo IDL.

Um servidor deve fornecer um EPV não **nulo** nos seguintes casos:

-   Quando os nomes das rotinas do Gerenciador forem diferentes dos nomes de procedimento declarados na definição de interface
-   Quando o servidor usa o EPV padrão para registrar outra implementação da interface

Um servidor declara um EPV do Gerenciador inicializando uma variável do tipo *If-name * * * \_ Server \_ EPV** para cada implementação da interface.

## <a name="registering-a-single-implementation-of-an-interface"></a>Registrando uma única implementação de uma interface

Quando um servidor oferece apenas uma implementação de uma interface, o servidor chama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) apenas uma vez. No caso padrão, o servidor usa o gerenciador padrão EPV. (A exceção é quando o gerente usa nomes de rotina que diferem daqueles declarados na interface.)

Para o caso padrão, forneça os seguintes valores para chamadas para [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2):

-   EPVs Manager

    Para usar o EPV padrão, especifique um valor **nulo** para o parâmetro *MgrEpv* .

-   UUID de tipo de Gerenciador

    Ao usar o EPV padrão, registre a interface com um UUID de tipo de Gerenciador nil fornecendo um valor **nulo** ou um UUID nil para o *MgrTypeUuid* um parâmetro. Nesse caso, todas as chamadas de procedimento remoto, independentemente do UUID do objeto em seu identificador de associação, são expedidas para o EPV padrão, supondo que nenhuma chamada [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) tenha sido feita.

    Você também pode fornecer um UUID de tipo de Gerenciador não nil. Nesse caso, você também deve chamar a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

## <a name="registering-multiple-implementations-of-an-interface"></a>Registrando várias implementações de uma interface

Você pode fornecer mais de uma implementação dos procedimentos remotos especificados no arquivo IDL. O aplicativo de servidor chama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para MAPEAr UUIDs de objeto para tipos UUIDs e chama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para associar a EPVs do Gerenciador a um UUID de tipo. Quando uma chamada de procedimento remoto chega com seu UUID de objeto, a biblioteca de tempo de execução do servidor RPC mapeia o UUID do objeto para um UUID de tipo. Em seguida, o aplicativo de servidor usa o UUID de tipo e o UUID de interface para selecionar o EPV do Gerenciador.

Você também pode especificar sua própria função para resolver o mapeamento do UUID do objeto para o UUID do tipo de Gerenciador. Você especifica a função de mapeamento ao chamar [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn).

Para oferecer várias implementações de uma interface, um servidor deve registrar cada implementação chamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) separadamente. Para cada implementação que um servidor registra, ele fornece o mesmo *IfSpec* um parâmetro, mas um par diferente de *MgrTypeUuid* e *MgrEpv* de parâmetros.

No caso de vários gerenciadores, use [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) da seguinte maneira:

-   EPVs Manager

    Para oferecer várias implementações de uma interface, um servidor deve:

    -   Crie um EPV de Gerenciador não **nulo** para cada implementação adicional.
    -   Especifique um valor não **nulo** para o *MgrEpv* de um parâmetro em [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

    Observe que o servidor também pode se registrar com o gerenciador padrão EPV.

-   UUID de tipo de Gerenciador

    Forneça um UUID de tipo de Gerenciador para cada EPV da interface. O UUID de tipo nil (ou valor **nulo** ) para o *MgrTypeUuid* um parâmetro pode ser especificado para um dos EPVs do Gerenciador. Cada UUID de tipo deve ser diferente.

## <a name="rules-for-invoking-manager-routines"></a>Regras para invocar rotinas do Gerenciador

A biblioteca de tempo de execução RPC despacha uma chamada de procedimento remoto de entrada para um gerente que oferece a interface RPC solicitada. Quando vários gerenciadores são registrados para uma interface, a biblioteca de tempo de execução RPC deve selecionar um deles. Para selecionar um gerente, a biblioteca de tempo de execução RPC usa o UUID do objeto especificado pelo identificador de ligação da chamada.

A biblioteca de tempo de execução aplica as seguintes regras ao interpretar o UUID de objeto de uma chamada de procedimento remoto:

-   UUIDs de objeto nil

    Um UUID de objeto nil é atribuído automaticamente ao UUID de tipo nil (é ilegal especificar um UUID de objeto nil na rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) ). Portanto, uma chamada de procedimento remoto cujo identificador de associação contém um UUID de objeto nil é automaticamente expedido para o Gerenciador registrado com o UUID de tipo nil, se houver.

-   UUIDs de objeto não nulos

    Em princípio, uma chamada de procedimento remoto cujo identificador de associação contém um UUID de objeto não nil deve ser processado por um gerente cujo UUID de tipo corresponde ao tipo do UUID do objeto. No entanto, identificar o Gerenciador correto requer que o servidor tenha especificado o tipo do UUID do objeto chamando a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    Se um servidor falhar ao chamar a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para um UUID de objeto não nulo, uma chamada de procedimento remoto para esse UUID de objeto passará para o Gerenciador EPV que faz chamadas de procedimento remoto de um UUID de objeto nulo (ou seja, o UUID de tipo nil).

    Chamadas de procedimento remoto com um UUID de objeto não nil no identificador de associação não poderão ser executadas se o servidor tiver atribuído esse UUID de objeto não nil a um UUID de tipo chamando a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) , mas também não registrou um EPV Manager para esse UUID de tipo chamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

A tabela a seguir resume as ações que a biblioteca de tempo de execução usa para selecionar a rotina do Gerenciador.



| UUID de objeto de chamada | Tipo de conjunto de servidores para UUID de objeto? | O servidor registrou o tipo EPV? | Ação de expedição                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Apostar                 | Não aplicável                   | Sim                         | Usa o Gerenciador com o UUID de tipo nil.                                                                                                           |
| Apostar                 | Não aplicável                   | Não                          | Erro (tipo de RPC \_ S \_ sem suporte \_ ); rejeita a chamada de procedimento remoto.                                                                              |
| Não nil             | Sim                              | Sim                         | Usa o Gerenciador com o mesmo UUID de tipo.                                                                                                          |
| Não nil             | Não                               | Ignored                     | Usa o Gerenciador com o UUID de tipo nil. Se nenhum Gerenciador com o UUID de tipo nil, erro (RPC \_ S \_ sem suporte); rejeita a chamada de procedimento remoto. |
| Não nil             | Sim                              | Não                          | Erro (RPC \_ S \_ sem suporte); rejeita a chamada de procedimento remoto.                                                                                |



 

O UUID do objeto da chamada é o UUID do objeto encontrado em um identificador de associação para uma chamada de procedimento remoto.

O servidor define o tipo do UUID de objeto chamando [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para especificar o UUID de tipo para um objeto.

O servidor registra o tipo para o Gerenciador de EPV chamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RPCSERVERREGISTERIF2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) usando o mesmo tipo uuid.

> [!Note]  
> O UUID do objeto nil sempre é atribuído automaticamente ao UUID do tipo nil. É ilegal especificar um UUID de objeto nil na rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Expedindo uma chamada de procedimento remoto para uma rotina do Gerenciador de servidores

As tabelas a seguir mostram as etapas que a biblioteca de tempo de execução RPC leva para distribuir uma chamada de procedimento remoto para uma rotina do Gerenciador de servidores.

Um caso simples em que o servidor registra o gerenciador padrão EPV, é descrito nas tabelas a seguir.

**Tabela de registro de interface**



| UUID de interface | UUID de tipo de Gerenciador | Vetor de ponto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Apostar               | EPV padrão        |



 

**Tabela de registro de objeto**



| UUID do objeto             | Tipo de objeto |
|-------------------------|-------------|
| Apostar                     | Apostar         |
| (Qualquer outro UUID de objeto) | Apostar         |



 

**Mapeando o identificador de associação para um vetor de ponto de entrada (EPV)**



| UUID de interface (do identificador de associação de cliente) | UUID de objeto (do identificador de associação de cliente) | Tipo de objeto (da tabela de registro de objeto) | EPV Manager (da tabela de registro de interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Apostar                                      | Apostar                                      | EPV padrão                                 |
| O mesmo que o descrito acima                               | *uuida*                                  | Apostar                                      | EPV padrão                                 |



 

As etapas a seguir descrevem as ações que a biblioteca de tempo de execução do servidor RPC assume, conforme mostrado nas tabelas anteriores, quando um cliente com interface UUID *uuid1* a chama.

1.  O servidor chama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para associar uma interface que ele oferece com o UUID de tipo de Gerenciador nil e com o gerenciador padrão gerado por MIDL EPV. Essa chamada adiciona uma entrada na tabela de registro da interface. O UUID de interface está contido no parâmetro *IfSpec* .
2.  Por padrão, a tabela de registro de objeto associa todos os UUIDs de objeto ao UUID de tipo nil. Neste exemplo, o servidor não chama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).
3.  A biblioteca de tempo de execução do servidor recebe um código de procedimento remoto que contém o UUID da interface ao qual a chamada pertence e o UUID do objeto do identificador de associação da chamada.

    Consulte as seguintes entradas de referência de função para discussões sobre como um UUID de objeto é definido em um identificador de associação:

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  Usando o UUID de interface da chamada de procedimento remoto, a biblioteca de tempo de execução do servidor localiza esse UUID de interface na tabela de registro da interface.

    Se o servidor não registrou a interface usando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2), a chamada de procedimento remoto retorna ao chamador com um RPC \_ S \_ desconhecido se o \_ código de status.

5.  Usando o UUID de objeto do identificador de associação, a biblioteca de tempo de execução do servidor localiza esse UUID de objeto na tabela de registro de objeto. Neste exemplo, todos os UUIDs de objeto são mapeados para o tipo de objeto nil.
6.  A biblioteca de tempo de execução do servidor localiza o tipo de Gerenciador nil na tabela de registro da interface.
7.  A combinação do UUID de interface e do tipo nil na tabela de registro de interface resolve para o EPV padrão, que contém as rotinas do Gerenciador de servidores a serem executadas para o UUID da interface encontrado na chamada de procedimento remoto.

Suponha que o servidor ofereça várias interfaces e várias implementações de cada interface, conforme descrito nas tabelas a seguir.

**Tabela de registro de interface**



| UUID de interface | UUID de tipo de Gerenciador | Vetor de ponto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Apostar               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Tabela de registro de objeto**



| UUID do objeto      | Tipo de objeto |
|------------------|-------------|
| *uuida*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *uuidd*          | *uuid3*     |
| *uuide*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| Apostar              | Apostar         |
| (Qualquer outro UUID) | Apostar         |



 

**Mapeando o identificador de associação para um vetor de ponto de entrada**



| UUID de interface (do identificador de associação de cliente) | UUID de objeto (do identificador de associação de cliente) | Tipo de objeto (da tabela de registro de objeto) | EPV Manager (da tabela de registro de interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Apostar                                      | Apostar                                      | *epv1*                                      |
| *uuid1*                                     | *uuida*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidd*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuide*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

As etapas a seguir descrevem as ações que a biblioteca de tempo de execução do servidor assume, conforme mostrado nas tabelas anteriores quando um cliente com interface UUID *uuid2* e Object UUID *uuidC* o chama.

1.  O servidor chama [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para associar as interfaces que ele oferece com o EPVs do Gerenciador diferente. As entradas na tabela de registro da interface refletem quatro chamadas de [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para oferecer duas interfaces, com duas implementações (EPVs) para cada interface.
2.  O servidor chama [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para estabelecer o tipo de cada objeto que ele oferece. Além da associação padrão do objeto nil a um tipo nil, todos os outros UUIDs de objeto não explicitamente encontrados na tabela de registro de objeto também são mapeados para o UUID de tipo nil.

    Neste exemplo, o servidor chama a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) seis vezes.

3.  A biblioteca de tempo de execução do servidor recebe uma chamada de procedimento remoto que contém o UUID da interface ao qual a chamada pertence e um UUID de objeto do identificador de associação da chamada.
4.  Usando o UUID de interface da chamada de procedimento remoto, a biblioteca de tempo de execução do servidor localiza o UUID da interface na tabela do registro da interface.
5.  Usando o UUID do objeto *uuidC* do identificador de associação, a biblioteca de tempo de execução do servidor localiza o UUID do objeto na tabela de registro de objeto e descobre que ele é mapeado para o tipo *uuid7*.
6.  Para localizar o tipo de Gerenciador, a biblioteca de tempo de execução do servidor combina o UUID de interface, *uuid2*, e o tipo *uuid7* na tabela de registro da interface. Isso resolve para *epv3*, que contém a rotina do Gerenciador do servidor a ser executada para a chamada de procedimento remoto.

As rotinas em *epv2* nunca serão executadas porque o servidor não chamou a rotina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para adicionar objetos com um UUID de tipo de *uuid4* à tabela de registro de objeto.

Uma chamada de procedimento remoto com interface UUID *uuid2* e Object UUID *uuidF* retorna ao chamador com um código de status de tipo de Gerenciador desconhecido de RPC S, \_ \_ \_ \_ pois o servidor não chamou [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para registrar a interface com um tipo de gerente de *uuid8*.

## <a name="return-values"></a>Valores de retorno

Essa função retorna um dos valores a seguir.



| Valor                             | Significado                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ OK                        | Sucesso                      |
| tipo de RPC \_ S \_ \_ já \_ registrado | UUID de tipo já registrado |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Fornecendo seu próprio objeto-função de consulta

Considere um servidor que gerencia milhares de objetos de muitos tipos diferentes. Sempre que o servidor for iniciado, o aplicativo de servidor precisaria chamar a função [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para cada um dos objetos, mesmo que os clientes possam se referir a apenas alguns deles (ou demoram muito para se referir a eles). Esses milhares de objetos provavelmente estarão no disco, portanto, recuperar seus tipos levaria tempo demorado. Além disso, a tabela interna que está mapeando o UUID do objeto para o UUID do tipo de Gerenciador iria, essencialmente, duplicar o mapeamento mantido com os próprios objetos.

Para sua conveniência, o conjunto de funções RPC inclui a função [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn). Com essa função, você fornece sua própria função de consulta de objeto.

Como exemplo, você pode fornecer sua própria função de consulta de objeto ao mapear objetos 100 – 199 para o tipo número 1, 200 – 299 para o tipo número 2 e assim por diante. A função de consulta de objeto também pode ser estendida para um sistema de arquivos distribuído, no qual o aplicativo de servidor não tem uma lista de todos os arquivos (UUIDs de objeto) disponíveis, ou quando os UUIDs de objeto nomeam arquivos no sistema de arquivos e você não deseja pré-carregar todos os mapeamentos entre UUIDs de objetos e tipos UUIDs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 




