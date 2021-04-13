---
title: Auxiliares de implementação do servidor fora do processo
description: Auxiliares de implementação do servidor fora do processo
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366769"
---
# <a name="out-of-process-server-implementation-helpers"></a>Auxiliares de implementação do servidor fora do processo

Quatro funções auxiliares que podem ser chamadas por servidores fora do processo estão disponíveis para simplificar o trabalho de escrever código de servidor. Os clientes COM e os servidores em processo normalmente não os chamaria. Essas funções foram projetadas para ajudar a evitar condições de corrida na ativação do servidor quando os servidores tiverem vários objetos Apartments ou várias classes. No entanto, eles também podem ser usados facilmente para servidores de objeto de classe única e de thread único. As funções são as seguintes:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Para desligar corretamente, um servidor COM deve controlar quantas instâncias de objeto ele criou e quantas vezes seu método [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) foi chamado. Somente quando ambas as contagens atingem zero, um servidor é desligado. Em servidores COM de thread único, a decisão de desligar foi coordenada com solicitações de ativação de entrada, que foram serializadas pela fila de mensagens. O servidor, após receber uma versão em sua instância de objeto final e decidir desligar, revogaria seus objetos de classe antes de qualquer solicitação de ativação ser expedida. Se uma solicitação de ativação chegasse depois desse ponto, o COM reconheceria que os objetos de classe foram revogados e retornariam um erro ao SCM (Gerenciador de controle de serviço), o que faria com que uma nova instância do processo do servidor local fosse executada.

No entanto, em um servidor de modelo de apartamento, no qual objetos de classe diferentes são registrados em diferentes Apartments, e em todos os servidores de thread livre, essa decisão para desligar deve ser coordenada com solicitações de ativação em vários threads para que um thread do servidor não decida desligar enquanto outro thread do servidor estiver ocupado a distribuir objetos de classe ou instâncias de objeto. Uma abordagem clássica, mas complicada, de resolver isso é ter o servidor, depois de revogar seus objetos de classe, verificar sua contagem de instâncias e permanecer ativa até que todas as instâncias tenham sido liberadas.

Para tornar mais fácil para os gravadores de servidor lidar com esses tipos de condições de corrida, o COM fornece duas funções de contagem de referência:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) incrementa uma contagem de referência global por processo.
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) decrementa a contagem de referência global por processo.

Quando a contagem de referência global por processo atinge zero, o COM chama automaticamente [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects), o que impede a entrada de novas solicitações de ativação. O servidor pode então cancelar o registro de seus vários objetos de classe de seus vários threads a lazer sem se preocupar que outra solicitação de ativação pode vir. Todas as novas solicitações de ativação são daqui em diante tratadas pelo SCM que inicia uma nova instância do processo do servidor local.

A maneira mais simples de um aplicativo de servidor local fazer uso dessas funções é chamar [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) no construtor para cada um de seus objetos de instância e em cada um de seus métodos [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) quando o parâmetro *Flock* é **true**. O aplicativo de servidor também deve chamar [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) no destruidor de cada um de seus objetos de instância e em cada um de seus métodos IClassFactory::**LockServer** quando o parâmetro *Flock* é **false**.

Por fim, o aplicativo de servidor deve prestar atenção ao código de retorno de [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)e, se ele retornar 0, o aplicativo de servidor deverá iniciar sua limpeza, que, para um servidor com vários threads, normalmente significa que ele deve sinalizar seus vários threads para sair de seus loops de mensagem e chamar [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) e [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess). Se as funções de gerenciamento de tempo de vida do processo do servidor forem usadas, elas deverão ser usadas nas duas instâncias de objeto e no método [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) ; caso contrário, o aplicativo de servidor pode ser desligado prematuramente.

Quando uma solicitação [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) é feita, o com contata o servidor, realiza marshaling da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) do objeto Class, retorna ao processo do cliente, desempacota a interface **IClassFactory** e retorna isso ao cliente. Neste ponto, os clientes normalmente chamam [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) com **true** para impedir que o processo do servidor seja desligado. No entanto, há uma janela de tempo entre quando o objeto de classe é empacotado e quando o cliente chama **LockServer** em que outro cliente pode se conectar ao mesmo servidor, obter uma instância e liberar essa instância, fazendo com que o servidor seja desligado e deixando o primeiro cliente alto e seco com um ponteiro **IClassFactory** desconectado. Para evitar essa condição de corrida, COM adiciona uma chamada implícita para **LockServer** com **true** para o objeto de classe quando ele realiza marshaling da interface **IClassFactory** e uma chamada implícita para **LockServer** com **false** quando o cliente libera a interface **IClassFactory** . Portanto, não é necessário fazer chamadas de **LockServer** remotas para o servidor e o proxy para **LockServer** simplesmente retorna S \_ OK sem realmente fazer a chamada de forma remota.

Há outra condição de corrida relacionada à ativação durante a inicialização de um processo de servidor fora do processo. Um servidor COM que registra várias classes normalmente chama [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com o \_ servidor local REGCLS \_ para cada CLSID compatível. Depois de fazer isso para todas as classes, o servidor entra em seu loop de mensagem. Para um servidor COM de thread único, todas as solicitações de ativação são bloqueadas até que o servidor insira o loop de mensagem. No entanto, para um servidor de modelo de apartamento que registra objetos de classe diferentes em diferentes Apartments e para todos os servidores de thread livre, as solicitações de ativação podem chegar antes disso. No caso de servidores de modelo de apartamento, as solicitações de ativação podem chegar assim que um thread tiver inserido seu loop de mensagem. No caso de servidores de thread livre, uma solicitação de ativação pode chegar assim que o primeiro objeto de classe é registrado. Como uma ativação pode ocorrer no início, também é possível que a versão final ocorra (e, portanto, fazer com que o servidor comece a ser desligado) antes que o restante do servidor tenha a chance de concluir a inicialização.

Para eliminar essas condições de corrida e simplificar o trabalho do Server Writer, qualquer servidor que queira registrar vários objetos de classe com com deve chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com o \_ servidor local REGCLS \_ \| REGCLS \_ suspenso para cada CLSID diferente ao qual o servidor dá suporte. Depois que todas as classes tiverem sido registradas e o processo do servidor estiver pronto para aceitar solicitações de ativação de entrada, o servidor deverá fazer uma chamada para [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects). Essa função informa ao COM para informar ao SCM sobre todas as classes registradas e começa a permitir que as solicitações de ativação no processo do servidor. O uso dessas funções oferece as seguintes vantagens:

-   Apenas uma chamada é feita ao SCM, independentemente de quantos CLSIDs são registrados, reduzindo assim o tempo de registro geral (e, portanto, o tempo de inicialização do aplicativo de servidor).
-   Se o servidor tiver vários Apartments e CLSIDs diferentes forem registrados em diferentes Apartments, ou se o servidor for um servidor de thread livre, nenhuma solicitação de ativação será exibida até que o servidor chame [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects), dando ao servidor uma oportunidade de registrar todos os seus CLSIDs e configurá-los corretamente antes de ter que lidar com solicitações de ativação e possíveis solicitações de desligamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 