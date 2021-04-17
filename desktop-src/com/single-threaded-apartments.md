---
title: Single-Threaded Apartments
description: Single-Threaded Apartments
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366750"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Apartments

O uso de Apartments de thread único (o processo de modelo de apartamento) oferece um paradigma baseado em mensagem para lidar com vários objetos executados simultaneamente. Ele permite que você escreva código mais eficiente, permitindo um thread, enquanto ele aguarda a conclusão de uma operação demorada, para permitir que outro thread seja executado.

Cada thread em um processo que é inicializado como um processo de modelo de apartamento, e que recupera e despacha mensagens de janela, é um thread apartment de thread único. Cada thread reside em seu próprio apartamento. Em um apartamento, os ponteiros de interface podem ser passados sem marshaling e, portanto, todos os objetos em um thread apartment de thread único se comunicam diretamente.

Um agrupamento lógico de objetos relacionados que todos executam no mesmo thread e, portanto, deve ter execução síncrona, pode residir no mesmo thread apartment de thread único. No entanto, um objeto de modelo de apartamento não pode residir em mais de um thread. As chamadas para objetos em outros threads devem ser feitas dentro do contexto do thread proprietário, portanto, os threads de comutadores COM distribuídos para você automaticamente quando você chama em um proxy.

Os modelos entre processos e interthread são semelhantes. Quando é necessário passar um ponteiro de interface para um objeto em outro apartamento (em outro thread) dentro do mesmo processo, você usa o mesmo modelo de marshaling que os objetos em processos diferentes usam para passar ponteiros entre limites de processo. Ao obter um ponteiro para o objeto de marshaling padrão, você pode realizar marshaling de ponteiros de interface entre limites de thread (entre Apartments) da mesma maneira que faz entre processos. (Os ponteiros de interface devem ser empacotados quando passados entre Apartments.)

Regras para Apartments de thread único são simples, mas é importante segui-las com cuidado:

-   Cada objeto deve residir em apenas um thread (dentro de um apartamento de thread único).
-   Inicialize a biblioteca COM para cada thread.
-   Realize marshaling de todos os ponteiros para objetos ao passá-los entre Apartments.
-   Cada apartamento de thread único deve ter um loop de mensagem para manipular chamadas de outros processos e Apartments dentro do mesmo processo. Apartments de thread único sem objetos (somente cliente) também precisam de um loop de mensagem para enviar as mensagens de difusão que alguns aplicativos usam.
-   Os objetos baseados em DLL ou em processo não chamam as funções de inicialização de COM; em vez disso, eles registram seu modelo de Threading com o **ThreadingModel** chamado-value na chave [InprocServer32](inprocserver32.md) no registro. Os objetos com reconhecimento de apartamento também devem gravar pontos de entrada de DLL com cuidado. Há considerações especiais que se aplicam aos servidores de Threading em processo. Para obter mais informações, consulte [problemas de thread de servidor em processo](in-process-server-threading-issues.md).

Embora vários objetos possam residir em um único thread, nenhum objeto de modelo Apartment pode residir em mais de um thread.

Cada thread de um processo de cliente ou servidor fora do processo deve chamar [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), ou chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) e especificar \_ APARTMENTTHREADED para o parâmetro *dwCoInit* . O apartamento principal é o thread que chama **CoInitializeEx** primeiro. Para obter informações sobre servidores em processo, consulte [problemas de Threading do servidor em processo](in-process-server-threading-issues.md).

Todas as chamadas para um objeto devem ser feitas em seu thread (dentro de seu apartamento). É proibido chamar um objeto diretamente de outro thread; usar objetos dessa maneira de thread livre pode causar problemas para aplicativos. A implicação dessa regra é que todos os ponteiros para objetos devem ser empacotados quando passados entre Apartments. COM fornece as duas funções a seguir para essa finalidade:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) empacota uma interface em um objeto de fluxo que é retornado para o chamador.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) desempacota um ponteiro de interface de um objeto de fluxo e o libera.

Essas funções encapsulam chamadas para as funções [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , que exigem o uso do \_ sinalizador InProc MSHCTX.

Em geral, o marshaling é realizado automaticamente pelo COM. Por exemplo, ao passar um ponteiro de interface como um parâmetro em uma chamada de método em um proxy para um objeto em outro apartamento, ou ao chamar [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), com faz o marshaling automaticamente. No entanto, em alguns casos especiais, em que o gravador de aplicativos está passando ponteiros de interface entre Apartments sem usar os mecanismos COM normais, o gravador deve tratar o marshaling manualmente.

Se um apartamento (apartamento 1) em um processo tiver um ponteiro de interface e outro apartamento (apartamento 2) exigir seu uso, o apartamento 1 deverá chamar [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) para realizar marshaling da interface. O fluxo criado por essa função é thread-safe e deve ser armazenado em uma variável acessível pelo apartamento 2. O apartamento 2 deve passar esse fluxo para [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) para desempacotar a interface e receberá um ponteiro para um proxy por meio do qual ele pode acessar a interface. O apartamento principal deve permanecer ativo até que o cliente tenha concluído todo o trabalho COM (porque alguns objetos em processo são carregados no apartamento principal, conforme descrito em [problemas de threading de servidor em processo](in-process-server-threading-issues.md)). Depois que um objeto é passado entre threads dessa maneira, é muito fácil passar ponteiros de interface como parâmetros. Dessa forma, Distributed COM faz o marshaling e a alternância de threads para o aplicativo.

Para lidar com chamadas de outros processos e Apartments no mesmo processo, cada apartamento de thread único deve ter um loop de mensagem. Isso significa que a função de trabalho do thread deve ter um loop GetMessage/DispatchMessage. Se outros primitivos de sincronização estiverem sendo usados para comunicação entre threads, a função [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) poderá ser usada para aguardar as mensagens e os eventos de sincronização de thread. A documentação para essa função tem um exemplo desse tipo de loop de combinação.

COM cria uma janela oculta usando a classe do Windows "OleMainThreadWndClass" em cada apartamento de thread único. Uma chamada para um objeto é recebida como uma mensagem de janela para esta janela oculta. Quando o apartamento do objeto recupera e despacha a mensagem, a janela oculta a receberá. O procedimento de janela Então chamará o método de interface correspondente do objeto.

Quando vários clientes chamarem um objeto, as chamadas serão enfileiradas na fila de mensagens e o objeto receberá uma chamada cada vez que seu apartamento recuperar e enviar mensagens. Como as chamadas são sincronizadas pelo COM e as chamadas são sempre entregues pelo thread que pertence ao apartamento do objeto, as implementações de interface do objeto não precisam fornecer sincronização. Apartments de thread único podem implementar [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para permitir que eles cancelem chamadas ou recebam mensagens de janela quando necessário.

O objeto poderá ser reinserido se uma de suas implementações de método de interface recuperar e despachar mensagens ou fizer uma chamada ORPC para outro thread, fazendo com que outra chamada seja entregue ao objeto (pelo mesmo apartamento). O OLE não impede a reentrância no mesmo thread, mas pode ajudar a fornecer segurança de thread. Isso é idêntico ao modo como um procedimento de janela pode ser reinserido se recuperar e despachar mensagens durante o processamento de uma mensagem. No entanto, chamar um servidor Apartment de thread único fora do processo que chama outro servidor Apartment de thread único permitirá que o primeiro servidor seja reinserido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Escolhendo o modelo de Threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartments multithread](multithreaded-apartments.md)
</dt> <dt>

[Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 