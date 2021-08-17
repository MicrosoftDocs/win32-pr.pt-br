---
description: As tabelas a seguir descrevem \_ as opções de soquete IPX NSPROTO que se aplicam aos soquetes criados para a família de endereços IPX/SPX (AF \_ IPX). Consulte as páginas de referência de função getsockopt e setsockopt para obter mais informações sobre como obter e definir opções de soquete.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: Opções de soquete NSPROTO_IPX (Wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6803b5ab6cdf3002a60726c30648a1ae61bb59430820f049aeb8b011f367e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993626"
---
# <a name="nsproto_ipx-socket-options"></a>\_Opções de soquete IPX NSPROTO

As tabelas a seguir descrevem as opções de soquete **\_ IPX NSPROTO** que se aplicam aos soquetes criados para a família de endereços IPX/SPX (AF \_ IPX). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**\_Opções de soquete IPX NSPROTO**</dt> <dd> <dl> <dt> 

| Opção                      | Obter | Definir | Tipo de optval                  | Descrição                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Endereço IPX                | sim |     | **\_dados de Endereço IPX \_**       | Retorna informações sobre o adaptador específico no qual o IPX está habilitado.                                                                                                                                                                                                          |
| \_notificação de Endereço IPX \_        | sim |     | **\_dados de Endereço IPX \_**       | Notifica de forma assíncrona quando o status de um adaptador IPX é alterado.                                                                                                                                                                                                              |
| \_DSTYPE IPX                 | sim | sim | DWORD                        | Obtém ou define o valor do campo Datastream no cabeçalho SPX para o qual enviar pacotes.                                                                                                                                                                                          |
| \_Endereço IPX estendido \_      |     | sim | DWORD (booliano)              | Habilita a opção de endereçamento estendido em pacotes IPX.                                                                                                                                                                                                                          |
| \_FILTERPTYPE IPX            | sim | sim | DWORD                        | Obtém ou define o tipo de pacote de filtro de recebimento IPX atual. Somente pacotes IPX com um tipo de pacote igual ao valor especificado no parâmetro optval serão retornados. Os pacotes com um tipo de pacote que não corresponde são descartados. Isso só é aplicável a um soquete de datagrama. |
| \_GETNETINFO IPX             | sim |     | **\_dados de NETNUM IPX \_**        | Retorna informações sobre um número de rede IPX específico. O membro netnum da estrutura **de \_ \_ dados IPX netnum** deve ser definido como o número de rede IPX a ser retornado.                                                                                                     |
| \_NORIP GETNETINFO \_ IPX      | sim |     | **\_dados de NETNUM IPX \_**        | Retorna informações sobre um número de rede IPX específico sem enviar uma solicitação de RIP. O membro netnum da estrutura **de \_ \_ dados IPX netnum** deve ser definido como o número de rede IPX a ser retornado.                                                                       |
| \_IMMEDIATESPXACK IPX        |     | sim | DWORD (booliano)              | Se definido como **true**, não adie o envio de ACKs em uma conexão SPX.                                                                                                                                                                                                             |
| \_número máximo de \_ adaptador \_ IPX      | sim |     | DWORD                        | Retorna o número de adaptadores habilitados para IPX presente.                                                                                                                                                                                                                             |
| \_MaxSize IPX                | sim |     | DWORD                        | Retorna o tamanho máximo do datagrama IPX em bytes que pode ser enviado.                                                                                                                                                                                                                |
| \_PTYPE IPX                  | sim | sim | DWORD                        | Obtém ou define o tipo de pacote. O valor especificado no parâmetro optval será definido como o tipo de pacote em cada pacote IPX enviado deste soquete.                                                                                                                             |
| \_difusão de recebimento de IPX \_     |     | sim | DWORD (booliano)              | Se definido como **true**, receba pacotes IPX de difusão.                                                                                                                                                                                                                              |
| \_RECVHDR IPX                |     | sim | DWORD (booliano)              | Se definido como **true**, receba cabeçalhos de protocolo IPX com dados.                                                                                                                                                                                                                     |
| \_RERIPNETNUMBER IPX         | sim |     | **\_dados de NETNUM IPX \_**        | Retorna informações sobre um número de rede IPX especificado usando uma nova solicitação de RIP. O membro netnum da estrutura **de \_ \_ dados IPX netnum** deve ser definido como o número de rede IPX a ser retornado.                                                                            |
| \_SPXGETCONNECTIONSTATUS IPX | sim |     | **\_dados de SPXCONNSTATUS IPX \_** | Retorna informações sobre as estatísticas de soquete SPX conectadas.                                                                                                                                                                                                                |
| \_STOPFILTERPTYPE IPX        |     | sim | DWORD                        | Remove o filtro e interrompe a filtragem no tipo de pacote especificado no parâmetro optval.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Windows Suporte para opções de NSPROTO \_ IPX**</dt> <dd> <dl> <dt> 

| Opção                      | Windows Vista e posterior | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_Endereço IPX                |                         | x                   | x          | x            | x           | x             |
| NOTIFICAÇÃO DE ENDEREÇO IPX \_ \_        |                         | x                   | x          | x            | x           | x             |
| IPX \_ DSTYPE                 |                         | x                   | x          | x            | x           | x             |
| ENDEREÇO \_ ESTENDIDO IPX \_      |                         | x                   | x          | x            | x           | x             |
| IPX \_ FILTERPTYPE            |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO             |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO \_ NORIP      |                         | x                   | x          | x            | x           | x             |
| IPX \_ IMMEDIATESPXACK        |                         | x                   | x          | x            | x           | x             |
| IPX \_ MAX \_ ADAPTER \_ NUM      |                         | x                   | x          | x            | x           | x             |
| IPX \_ MAXSIZE                |                         | x                   | x          | x            | x           | x             |
| IPX \_ PTYPE                  |                         | x                   | x          | x            | x           | x             |
| IPX \_ RECEIVE \_ BROADCAST     |                         | x                   | x          | x            | x           | x             |
| IPX \_ RECVHDR                |                         | x                   | x          | x            | x           | x             |
| IPX \_ RERIPNETNUMBER         |                         | x                   | x          | x            | x           | x             |
| IPX \_ SPXGETCONNECTIONSTATUS |                         | x                   | x          | x            | x           | x             |
| IPX \_ STOPFILTERPTYPE        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

As seguintes opções de **soquete \_ IPX NSPROTO** foram definidas no Windows Sockets 2 Protocol-Specific Anexo, mas não são implementadas pelo protocolo Windows IPX/SPX.

*nível* **=** **NSPROTO \_ IPX**



| Opção           | Type | Padrão                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX \_ CHECKSUM    | Bool | Desligar                             | Quando definido, o IPX executa uma soma de verificação em pacotes de saída e verifica a soma de verificação de pacotes de entrada.                                                          |
| \_TXPKTSIZE IPX   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagrama de envio. Esse tamanho não inclui o cabeçalho IPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia.    |
| \_RXPKTSIZE IPX   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagramas de recebimento. Esse tamanho não inclui o cabeçalho IPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia. |
| \_TXMEDIASIZE IPX | INT  | Placa principal                   | Retorna o tamanho da mídia de envio que define um limite superior para o tamanho do datagrama.                                                                                       |
| \_RXMEDIASIZE IPX | INT  | Placa principal                   | Retorna o tamanho da mídia de recebimento que define um limite superior para o tamanho do datagrama.                                                                                    |
| IPX \_ primário     | Bool | Primário                         | Restringe o tráfego para a placa de rede primária.                                                                                                               |



 

as opções de soquete **NSPROTO \_ SPX** a seguir foram definidas no Windows sockets 2 Protocol-Specific anexo, mas não são implementadas em Windows pelo protocolo Windows IPX/SPX.

*nível* **=** do **NSPROTO \_ SPX**



| Opção           | Type | Padrão                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| soma de verificação do SPX \_    | Bool | Desligar                             | Quando definido, o IPX executa uma soma de verificação em pacotes de saída e verifica a soma de verificação de pacotes de entrada. Sem suporte em todas as plataformas.                          |
| SPX \_ TXPKTSIZE   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagrama de envio. Esse tamanho não inclui o cabeçalho SPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia.    |
| SPX \_ RXPKTSIZE   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagramas de recebimento. Esse tamanho não inclui o cabeçalho SPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia. |
| SPX \_ TXMEDIASIZE | INT  | Placa principal                   | Retorna o tamanho da mídia de envio menos o SPX e os cabeçalhos de mídia. Isso define um limite superior para o tamanho do pacote de segmentação de mensagem.                                       |
| SPX \_ RXMEDIASIZE | INT  | Placa principal                   | Retorna o tamanho da mídia de recebimento menos o SPX e os cabeçalhos de mídia. Isso define um limite superior para o tamanho do pacote de recebimento.                                                 |
| SPX \_ RAWSPX      | Bool | Desligar                             | Quando definido, o cabeçalho do protocolo IPX/SPX é passado com os dados.                                                                                                |



 

## <a name="remarks"></a>Comentários

As opções de soquete **\_ IPX NSPROTO** e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *Wsnwlink. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wsnwlink. h</dt> </dl> |



 

 




