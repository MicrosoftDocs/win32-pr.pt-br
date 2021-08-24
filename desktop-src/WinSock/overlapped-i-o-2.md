---
description: Windows Os soquetes 2 apresentam e/s sobreposta e exigem que todos os provedores de transporte ofereçam suporte a esse recurso.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Entrada/saída sobreposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641786"
---
# <a name="overlapped-inputoutput"></a>Entrada/saída sobreposta

Windows Os soquetes 2 apresentam e/s sobreposta e exigem que todos os provedores de transporte ofereçam suporte a esse recurso. A e/s sobreposta pode ser executada somente em soquetes que foram criados por meio da função [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) com o sinalizador de cabeçalho wsa \_ \_ sobreposto definido e seguir o modelo estabelecido em Windows.

Para receber, um cliente usa [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ou [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) para fornecer buffers para os quais os dados serão recebidos. Se um ou mais buffers forem lançados antes da hora em que os dados foram recebidos pela rede, será possível que os dados sejam colocados nos buffers do usuário imediatamente, conforme eles chegam e, portanto, evitem a operação de cópia que, caso contrário, ocorreria. Se os dados chegarem quando os buffers de recebimento já tiverem sido postados, eles serão copiados imediatamente para os buffers do usuário. Se os dados chegarem quando nenhum buffer de recebimento tiver sido postado pelo aplicativo, o provedor de serviços Resort para o estilo síncrono de operação em que os dados de entrada são armazenados em buffer internamente até o momento em que o cliente emite uma chamada de recebimento e, portanto, fornece um buffer no qual os dados podem ser copiados. Uma exceção a isso seria se o aplicativo usava [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) para definir o tamanho do buffer de recebimento como zero. Nessa instância, os protocolos confiáveis só permitirão que os dados sejam recebidos quando os buffers de aplicativo tivessem sido postados, e os dados em protocolos não confiáveis seriam perdidos.

No lado de envio, os clientes usam [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) ou [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) para fornecer ponteiros para os buffers preenchidos e, em seguida, concorda em não incomodar os buffers de forma alguma até que a rede consumisse o conteúdo do buffer.

Chamadas de envio e recebimento sobrepostas retornam imediatamente. Um valor de retorno de zero indica que a operação de e/s foi concluída imediatamente e que a indicação de conclusão correspondente já ocorreu. Ou seja, o objeto de evento associado foi sinalizado ou a rotina de conclusão foi enfileirada por meio de [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Um valor de retorno do \_ erro de soquete associado a um código de erro de WSA \_ e/s de cabeçalho \_ pendente indica que a operação sobreposta foi iniciada com êxito e que uma indicação subseqüente será fornecida quando os buffers de envio tiverem sido consumidos ou quando os buffers de recebimento forem preenchidos. Qualquer outro código de erro indica que a operação sobreposta não foi iniciada com êxito e que nenhuma indicação de conclusão estará disponível.

Ambas as operações de envio e recebimento podem ser sobrepostas. As funções Receive podem ser invocadas várias vezes para postar buffers de recebimento em preparação para dados de entrada, e as funções Send podem ser invocadas várias vezes para colocar em fila vários buffers a serem enviados. Observe que, embora uma série de buffers de envio sobrepostos seja enviada na ordem fornecida, as indicações de conclusão correspondentes podem ocorrer em uma ordem diferente. Da mesma forma, no lado de recebimento, os buffers serão preenchidos na ordem em que são fornecidos, mas as indicações de conclusão podem ocorrer em uma ordem diferente.

O recurso de conclusão adiada de e/s sobreposta também está disponível para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)).

## <a name="delivering-completion-indications"></a>Entrega de indicações de conclusão

Os provedores de serviço têm duas maneiras de indicar conclusão sobreposta: definir um objeto de evento especificado pelo cliente ou invocar uma rotina de conclusão especificada pelo cliente. Em ambos os casos, uma estrutura de dados, [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped), é associada a cada operação sobreposta. Essa estrutura é alocada pelo cliente e usada por ela para indicar qual objeto de evento (se houver) deve ser definido quando a conclusão ocorre. A estrutura **WSAOVERLAPPED** pode ser usada pelo provedor de serviços como um local para armazenar um identificador nos resultados (por exemplo, número de bytes transferidos, sinalizadores atualizados, códigos de erro, etc.) para uma operação sobreposta em particular. Para obter esses resultados, os clientes devem invocar [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), passando um ponteiro para a estrutura sobreposta correspondente.

Se a indicação de conclusão baseada em evento for selecionada para uma determinada solicitação de e/s sobreposta, a rotina [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) poderá ser usada por clientes para sondar ou aguardar a conclusão da operação sobreposta. Se a indicação de conclusão baseada em rotina de conclusão for selecionada para uma determinada solicitação de e/s sobreposta, somente a opção de sondagem de **WSPGetOverlappedResult** estará disponível. Um cliente também pode usar outros meios de aguardar (como usar [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)) até que o objeto de evento correspondente tenha sido sinalizado ou a rotina de conclusão especificada tenha sido invocada pelo provedor de serviços. Depois que a conclusão tiver sido indicada, o cliente poderá invocar **WSPGetOverlappedResult**, com a expectativa de que a chamada seja concluída imediatamente.

## <a name="invoking-socket-io-completion-routines"></a>Invocando rotinas de conclusão de e/s de soquete

Se o parâmetro *lpCompletionRoutine* para uma operação sobreposta não for **NULL**, será responsabilidade do provedor de serviço se organizar para invocar a rotina de conclusão especificada pelo cliente quando a operação sobreposta for concluída. Como a rotina de conclusão deve ser executada no contexto do mesmo thread que iniciou a operação sobreposta, ela não pode ser invocada diretamente do provedor de serviços. O \_32.DLL Ws2 oferece um mecanismo de chamada de procedimento assíncrono (APC) para facilitar a invocação de rotinas de conclusão.

Um provedor de serviços organiza uma função a ser executada no thread apropriado chamando [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Essa função pode ser chamada de qualquer contexto de processo e thread, até mesmo um contexto diferente do thread e do processo que foi usado para iniciar a operação sobreposta.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) usa como parâmetros de entrada um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) , um ponteiro para uma função APC a ser invocada e um valor de contexto de 32 bits que é posteriormente passado para a função APC. Provedores de serviço são sempre fornecidos com um ponteiro para a estrutura **WSATHREADID** apropriada por meio do parâmetro *lpThreadId* para a função Overlapped. O provedor deve armazenar a estrutura **WSATHREADID** localmente e fornecer um ponteiro para essa cópia da estrutura **WSATHREADID** como um parâmetro de entrada para **WPUQueueApc**. Depois que a função **WPUQueueApc** retorna, o provedor pode descartar sua cópia do **WSATHREADID**.

O procedimento [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) simplesmente enfileira informações suficientes para chamar a função APC indicada com os parâmetros fornecidos, mas não a chama. Quando o thread-alvo entra em um estado de espera alertável, essas informações são removidas da fila e uma chamada é feita à função APC nesse thread de destino e no contexto do processo. Como o mecanismo da APC dá suporte apenas a um único valor de contexto de 32 bits, a função APC não pode ser a rotina de conclusão especificada pelo cliente, que envolve mais parâmetros. Em vez disso, o provedor de serviços deve fornecer um ponteiro para sua própria função APC, que usa o valor de contexto fornecido para acessar as informações de resultado necessárias para a operação sobreposta e, em seguida, invoca a rotina de conclusão especificada pelo cliente.

Para provedores de serviços em que um componente de modo de usuário implementa e/s sobreposta, um uso típico do mecanismo da APC é o seguinte:

-   Quando a operação de e/s é concluída, o provedor aloca um buffer pequeno e o compacta com um ponteiro para o procedimento de conclusão fornecido pelo cliente e os valores de parâmetro a serem passados para o procedimento.
-   Ele enfileira uma APC, especificando o ponteiro para o buffer como o valor de contexto e seu próprio procedimento intermediário como o procedimento de destino.
-   Quando o thread-alvo eventualmente entra no estado de espera alertável, o procedimento intermediário do provedor de serviço é chamado no contexto de thread apropriado.
-   O procedimento intermediário simplesmente desempacota os parâmetros, desaloca o buffer e chama o procedimento de conclusão fornecido pelo cliente.
-   Para provedores de serviços em que um componente de modo kernel implementa e/s sobreposta, uma implementação típica é semelhante, exceto que a implementação usaria as interfaces de kernel padrão para enfileirar a APC.

a descrição das interfaces de kernel relevantes está fora do escopo da especificação Windows sockets 2.

> [!Note]  
> os provedores de serviços devem permitir que os clientes do Windows sockets 2 invoquem as operações de envio e recebimento de dentro do contexto da rotina de conclusão de e/s de soquete e garantir que, para um determinado soquete, as rotinas de conclusão de e/s não serão aninhadas.

 

Em algumas circunstâncias, um provedor de serviços em camadas pode precisar iniciar e concluir operações sobrepostas de dentro de um thread de trabalho interno. Nesse caso, um [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) não estaria disponível a partir de uma chamada de função de entrada. A interface do provedor de serviços fornece uma chamada, [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread), para obter um **WSATHREADID** para o thread atual. Quando esse **WSATHREADID** não for mais necessário, seus recursos deverão ser retornados chamando [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread).

 

 
