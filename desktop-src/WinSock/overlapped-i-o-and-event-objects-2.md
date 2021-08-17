---
description: Windows Os soquetes 2 são compatíveis com E/S sobressalo e todos os provedores de transporte são compatíveis com essa funcionalidade.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Objetos de evento e E/S sobre mapeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ae2ee17036275183518bfd444b9317bcdc05145a9fcb327ad48388618a66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741044"
---
# <a name="overlapped-io-and-event-objects"></a>Objetos de evento e E/S sobre mapeados

Windows Os soquetes 2 são compatíveis com E/S sobressalo e todos os provedores de transporte são compatíveis com essa funcionalidade. A E/S sobrecarretada segue o modelo estabelecido no Windows e pode [](/windows/desktop/api/Winsock2/nf-winsock2-socket) ser executada em soquetes criados com a função de soquete ou soquetes criados com a [**função WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o sinalizador **WSA \_ FLAG \_ OVERLAPPED** definido no parâmetro *dwFlags.*

> [!Note]  
> A criação de um soquete com o atributo sobrecodado não tem impacto sobre se um soquete está atualmente no modo de bloqueio ou não bloqueado. Soquetes criados com o atributo sobressalo podem ser usados para executar E/S sobressalo– fazer isso não altera o modo de bloqueio de um soquete. Como as operações de E/S sobressaladas não bloqueiam, o modo de bloqueio de um soquete é irrelevante para essas operações.

 

Para receber, os aplicativos usam as funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) para fornecer buffers nos quais os dados devem ser recebidos. Se um ou mais buffers são postados antes do momento em que os dados foram recebidos pela rede, esses dados podem ser colocados nos buffers do usuário imediatamente à medida que chegam. Portanto, ele pode evitar a operação de cópia que, de outra forma, ocorreria no momento em que a função [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) ou [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) é invocada. Se os dados já estão presentes quando buffers de recebimento são postados, eles são copiados imediatamente para os buffers do usuário.

Se os dados chegam quando nenhum buffer de recebimento foi postado pelo aplicativo, a rede recorre ao estilo síncrono familiar da operação. Ou seja, os dados de entrada são armazenados em buffer internamente até que o aplicativo emite uma chamada de recebimento e, assim, fornece um buffer no qual os dados podem ser copiados. Uma exceção a isso é quando o aplicativo usa [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir o tamanho do buffer de recebimento como zero. Nesse caso, os protocolos confiáveis só permitiriam que os dados sejam recebidos quando os buffers de aplicativos tivessem sido postados e os dados em protocolos não confiáveis seriam perdidos.

No lado do envio, os aplicativos usam [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) para fornecer ponteiros para buffers preenchidos e, em seguida, concordar em não interromper os buffers de nenhuma forma até que a rede tenha consumido o conteúdo do buffer.

As chamadas de envio e recebimento sobrecarradas retornam imediatamente. Um valor de retorno de zero indica que a operação de E/S foi concluída imediatamente e que a indicação de conclusão correspondente já ocorreu. Ou seja, o objeto de evento associado foi sinalizado ou uma rotina de conclusão foi en fila e será executada quando o thread de chamada entrar no estado de espera alertável.

Um valor de retorno de SOCKET ERROR juntamente com um código de erro de PENDING de E/S do \_ [WSA \_ \_ ](windows-sockets-error-codes-2.md) indica que a operação sobreexplorada foi iniciada com êxito e que uma indicação subsequente será fornecida quando buffers de envio foram consumidos ou quando uma operação de recebimento tiver sido concluída. No entanto, para soquetes que têm o estilo de fluxo de byte, a indicação de conclusão ocorre sempre que os dados de entrada são esgotados, independentemente de os buffers estar cheio. Qualquer outro código de erro indica que a operação sobrecarrável não foi iniciada com êxito e que nenhuma indicação de conclusão será futura.

As operações de envio e recebimento podem ser sobrecarradas. As funções de recebimento podem ser invocadas várias vezes para postar buffers de recebimento em preparação para dados de entrada, e as funções de envio podem ser invocadas várias vezes para enfil de vários buffers para enviar. Embora o aplicativo possa contar com uma série de buffers de envio sobrecarecidos que estão sendo enviados na ordem fornecida, as indicações de conclusão correspondentes podem ocorrer em uma ordem diferente. Da mesma forma, no lado do recebimento, os buffers podem ser preenchidos na ordem em que são fornecidos, mas as indicações de conclusão podem ocorrer em uma ordem diferente.

Em muitos casos, as operações sobrecarrecatadas do Winsock usando [**AcceptEx,**](/windows/win32/api/mswsock/nf-mswsock-acceptex) [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)e funções semelhantes são canceláveis. No entanto, o comportamento é indefinido para o uso contínuo de um soquete que cancelou operações pendentes. A [**função closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve ser chamada depois de cancelar uma operação sobrecarretada. Portanto, para melhores resultados, em vez de cancelar a E/S diretamente, a função **closesocket** deve ser chamada para fechar o soquete, o que acabará descontinuando todas as operações pendentes.

O recurso de conclusão adiada de E/S sobrecarretada também está disponível para [**WSAIoctl,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)que é uma versão aprimorada [**do ioctlsocket.**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

 

 
