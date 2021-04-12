---
title: Problemas de Threading do In-Process Server
description: Problemas de Threading do In-Process Server
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366908"
---
# <a name="in-process-server-threading-issues"></a>Problemas de Threading do In-Process Server

Um servidor em processo não chama [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)ou [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) para marcar seu modelo de Threading. Para objetos baseados em DLL ou em processo de reconhecimento de thread, você precisa definir o modelo de threading no registro. O modelo padrão quando você não especifica um modelo de threading é de thread único por processo. Para especificar um modelo, você adiciona o valor de **ThreadingModel** à chave [InprocServer32](inprocserver32.md) no registro.

DLLs que dão suporte à instanciação de um objeto de classe devem implementar e exportar as funções [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow). Quando um cliente deseja uma instância da classe à qual a DLL dá suporte, uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (diretamente ou por meio de uma chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chama **DllGetClassObject** para obter um ponteiro para seu objeto de classe quando o objeto é implementado em uma dll. O **DllGetClassObject** , portanto, deve ser capaz de fornecer vários objetos de classe ou um único objeto thread-safe (essencialmente, simplesmente usando [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) em suas contagens de referência internas).

Como o nome indica, [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) é chamado para determinar se a DLL que a implementa está em uso, permitindo que o chamador o descarregue com segurança, se não for. Chamadas para [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) de qualquer thread sempre roteiam o thread do apartamento principal para chamar **DllCanUnloadNow**.

Assim como outros servidores, os servidores em processo podem ser de thread único, de thread apartment ou de thread livre. Esses servidores podem ser usados por qualquer cliente OLE, independentemente do modelo de Threading usado pelo cliente.

Todas as combinações de interoperabilidade do modelo de Threading são permitidas entre clientes e objetos em processo. A interação entre um cliente e um objeto em processo que usa modelos de Threading diferentes é exatamente como a interação entre clientes e servidores fora do processo. Para um servidor em processo, quando o modelo de Threading do cliente e do servidor em processo difere, o COM deve se apresentar entre o cliente e o objeto.

Quando um objeto em processo que dá suporte ao modelo de thread único é chamado simultaneamente por vários threads de um cliente, o COM não pode permitir que os threads do cliente acessem diretamente o interfaceâ do objeto "o objeto não foi projetado para esse acesso. Em vez disso, COM deve garantir que as chamadas sejam sincronizadas e sejam feitas somente pelo thread do cliente que criou o objeto. Portanto, o COM cria o objeto no apartamento principal do cliente e requer que todos os outros Apartments do cliente acessem o objeto usando proxies.

Quando um apartamento de thread livre (modelo de apartamento multi-threaded) em um cliente cria um servidor em processo Apartment-Threaded, o COM gira um thread de "host" de modelo de apartamento de um único thread no cliente. Esse thread de host criará o objeto e o ponteiro de interface será submetido a marshaling de volta para o apartamento de thread livre do cliente. Da mesma forma, quando um apartamento de thread único em um cliente de modelo de apartamento cria um servidor de thread em processo livre, o COM gira um thread de host de thread livre (multithreaded apartment no qual o objeto será criado e, em seguida, é empacotado de volta para o apartamento de thread único do cliente).

> [!Note]  
> Em geral, se você criar uma interface personalizada em um servidor em processo, também deverá fornecer o código de marshaling para ela, de modo que o COM possa realizar marshaling da interface entre o cliente Apartments.

 

O COM ajuda a proteger o acesso a objetos fornecidos por uma DLL de thread único, exigindo acesso do mesmo apartamento de cliente no qual eles foram criados. Além disso, todos os pontos de entrada de DLL (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) e os dados globais devem ser sempre acessados pelo mesmo apartamento. O COM cria esses objetos no apartamento principal do cliente, dando ao principal o acesso direto do apartamento aos ponteiros do objeto. Chamadas de outro Apartments usam o marshaling entre threads para ir do proxy para o stub no apartamento principal e, em seguida, para o objeto. Isso permite que o COM sincronize chamadas para o objeto. Chamadas interthreads são lentas, portanto, é recomendável que esses servidores sejam reescritos para dar suporte a vários Apartments.

Como um servidor de thread único em processo, um objeto fornecido por uma DLL de modelo de apartamento deve ser acessado pelo mesmo apartamento de cliente do qual foi criado. No entanto, os objetos fornecidos por esse servidor podem ser criados em vários Apartments do cliente, portanto, o servidor deve implementar seus pontos de entrada (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) para uso multithread. Por exemplo, se dois Apartments de um cliente tentarem criar duas instâncias do objeto em processo simultaneamente, **DllGetClassObject** poderá ser chamado simultaneamente por ambos os Apartments. **DllCanUnloadNow** deve ser escrito para que a dll não seja descarregada enquanto o código ainda estiver sendo executado na dll.

Se a DLL fornecer apenas uma instância da fábrica de classes para criar todos os objetos, a implementação da fábrica de classes também deverá ser projetada para uso multithread, pois ela será acessada por vários clientes Apartments. Se a DLL criar uma nova instância da fábrica de classes cada vez que [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) for chamado, a fábrica de classes não precisará ser thread-safe.

Os objetos criados pela fábrica de classes não precisam ser thread-safe. Uma vez criado por um thread, o objeto é sempre acessado por meio desse thread e todas as chamadas para o objeto são sincronizadas pelo COM. O apartamento do modelo de apartamento de um cliente que cria esse objeto receberá um ponteiro direto para o objeto. Os Apartments de cliente que são diferentes do apartamento no qual o objeto foi criado devem acessar o objeto por meio de proxies. Esses proxies são criados quando o cliente realiza marshaling da interface entre seu Apartments.

Quando um valor de **ThreadingModel** de dll em processo é definido como "both", um objeto fornecido por essa DLL pode ser criado e usado diretamente (sem um proxy) em Apartments de cliente de thread único ou multithread. No entanto, ele só pode ser usado diretamente dentro do apartamento no qual foi criado. Para fornecer o objeto para qualquer outro apartamento, o objeto deve ser empacotado. O objeto DLL deve implementar sua própria sincronização e pode ser acessado por vários clientes Apartments ao mesmo tempo.

Para acelerar o desempenho de acesso de thread livre a objetos DLL em processo, o COM fornece a função [**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) . Essa função cria um objeto de marshaling com thread livre que pode ser agregado com um objeto de servidor em processo. Quando um apartamento de cliente no mesmo processo precisa de acesso a um objeto em outro apartamento, agregar o marshaler de thread livre fornece ao cliente um ponteiro direto para o objeto de servidor, em vez de um proxy, quando o cliente realiza o marshaling da interface do objeto para um apartamento diferente. O cliente não precisa fazer nenhuma sincronização. Isso funciona apenas dentro do mesmo processo; o marshaling padrão é usado para uma referência ao objeto que é enviado para outro processo.

Um objeto fornecido por uma DLL em processo que dá suporte apenas a threads livres é um objeto de thread livre. Ele implementa sua própria sincronização e pode ser acessado por vários threads de cliente ao mesmo tempo. Esse servidor não empacota interfaces entre threads, portanto, esse servidor pode ser criado e usado diretamente (sem um proxy) somente por Apartments de vários threads em um cliente. O Apartments de thread único que o cria acessará por meio de um proxy.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Escolhendo o modelo de Threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartments multithread](multithreaded-apartments.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 