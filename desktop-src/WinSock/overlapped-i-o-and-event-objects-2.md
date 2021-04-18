---
description: O Windows Sockets 2 dá suporte a e/s sobreposta e todos os provedores de transporte dão suporte a esse recurso.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Objetos de evento e e/s sobrepostos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781661"
---
# <a name="overlapped-io-and-event-objects"></a>Objetos de evento e e/s sobrepostos

O Windows Sockets 2 dá suporte a e/s sobreposta e todos os provedores de transporte dão suporte a esse recurso. A e/s sobreposta segue o modelo estabelecido no Windows e pode ser executada em soquetes criados com a função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou com soquetes criados com a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o sinalizador de **cabeçalho wsa \_ \_ sobreposto** definido no parâmetro *dwFlags* .

> [!Note]  
> A criação de um soquete com o atributo Overlapped não afeta se um soquete está atualmente no modo de bloqueio ou sem bloqueio. Os soquetes criados com o atributo Overlapped podem ser usados para executar e/s sobreposta — fazer isso não altera o modo de bloqueio de um soquete. Como as operações de e/s sobrepostas não são bloqueadas, o modo de bloqueio de um soquete é irrelevante para essas operações.

 

Para receber, os aplicativos usam as funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) para fornecer buffers para os quais os dados serão recebidos. Se um ou mais buffers forem postados antes do momento em que os dados tiverem sido recebidos pela rede, esses dados poderão ser colocados nos buffers do usuário imediatamente conforme ele chegar. Portanto, ele pode evitar a operação de cópia que, caso contrário, ocorreria no momento em que a função [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) ou [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) é invocada. Se os dados já estiverem presentes quando os buffers de recebimento forem postados, eles serão copiados imediatamente para os buffers do usuário.

Se os dados chegarem quando nenhum buffer de recebimento tiver sido postado pelo aplicativo, os resorts de rede para o estilo de operação síncrono conhecido. Ou seja, os dados de entrada são armazenados em buffer internamente até que o aplicativo emita uma chamada de recebimento e, portanto, forneça um buffer no qual os dados possam ser copiados. Uma exceção a isso é quando o aplicativo usa [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir o tamanho do buffer de recebimento como zero. Nessa instância, os protocolos confiáveis só permitiriam que os dados fossem recebidos quando os buffers de aplicativo tivessem sido postados e dados em protocolos não confiáveis seriam perdidos.

No lado de envio, os aplicativos usam [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) para fornecer ponteiros para os buffers preenchidos e, em seguida, concorda em não incomodar os buffers de forma alguma até que a rede consumisse o conteúdo do buffer.

Chamadas de envio e recebimento sobrepostas retornam imediatamente. Um valor de retorno de zero indica que a operação de e/s foi concluída imediatamente e que a indicação de conclusão correspondente já ocorreu. Ou seja, o objeto de evento associado foi sinalizado, ou uma rotina de conclusão foi enfileirada e será executada quando o thread de chamada chegar ao estado de espera alertável.

Um valor de retorno do \_ erro de soquete associado a um código de erro de [WSA \_ e/s de cabeçalho \_ pendente](windows-sockets-error-codes-2.md) indica que a operação sobreposta foi iniciada com êxito e que uma indicação subseqüente será fornecida quando os buffers de envio tiverem sido consumidos ou quando uma operação de recebimento tiver sido concluída. No entanto, para soquetes que são o estilo de fluxo de bytes, a indicação de conclusão ocorre sempre que os dados de entrada são esgotados, independentemente de os buffers estarem cheios ou não. Qualquer outro código de erro indica que a operação sobreposta não foi iniciada com êxito e que nenhuma indicação de conclusão estará disponível.

Ambas as operações de envio e recebimento podem ser sobrepostas. As funções Receive podem ser chamadas várias vezes para postar buffers de recebimento em preparação para dados de entrada, e as funções Send podem ser chamadas várias vezes para enfileirar vários buffers para enviar. Embora o aplicativo possa contar com uma série de buffers de envio sobrepostos sendo enviados na ordem fornecida, as indicações de conclusão correspondentes podem ocorrer em uma ordem diferente. Da mesma forma, no lado de recebimento, os buffers podem ser preenchidos na ordem em que são fornecidos, mas as indicações de conclusão podem ocorrer em uma ordem diferente.

Em muitos casos, as operações do Winsock Overlapped usando [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)e funções semelhantes são canceláveis. No entanto, o comportamento é indefinido para o uso contínuo de um soquete que cancelou operações pendentes. A função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve ser chamada depois de cancelar uma operação sobreposta. Portanto, para obter melhores resultados, em vez de cancelar a e/s diretamente, a função **fechamento** deve ser chamada para fechar o soquete, o que eventualmente interromperá todas as operações pendentes.

O recurso de conclusão adiada de e/s sobreposta também está disponível para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), que é uma versão aprimorada do [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
