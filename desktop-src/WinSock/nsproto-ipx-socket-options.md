---
description: As tabelas a seguir descrevem \_ as opções de soquete IPX NSPROTO que se aplicam aos soquetes criados para a família de endereços IPX/SPX (AF \_ IPX). Consulte as páginas de referência de função getsockopt e setsockopt para obter mais informações sobre como obter e definir opções de soquete.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: Opções de soquete NSPROTO_IPX (Wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748092"
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



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Suporte do Windows para \_ Opções de IPX NSPROTO**</dt> <dd> <dl> <dt> 

| Opção                      | Windows Vista e posterior | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_Endereço IPX                |                         | x                   | x          | x            | x           | x             |
| \_notificação de Endereço IPX \_        |                         | x                   | x          | x            | x           | x             |
| \_DSTYPE IPX                 |                         | x                   | x          | x            | x           | x             |
| \_Endereço IPX estendido \_      |                         | x                   | x          | x            | x           | x             |
| \_FILTERPTYPE IPX            |                         | x                   | x          | x            | x           | x             |
| \_GETNETINFO IPX             |                         | x                   | x          | x            | x           | x             |
| \_NORIP GETNETINFO \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_IMMEDIATESPXACK IPX        |                         | x                   | x          | x            | x           | x             |
| \_número máximo de \_ adaptador \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_MaxSize IPX                |                         | x                   | x          | x            | x           | x             |
| \_PTYPE IPX                  |                         | x                   | x          | x            | x           | x             |
| \_difusão de recebimento de IPX \_     |                         | x                   | x          | x            | x           | x             |
| \_RECVHDR IPX                |                         | x                   | x          | x            | x           | x             |
| \_RERIPNETNUMBER IPX         |                         | x                   | x          | x            | x           | x             |
| \_SPXGETCONNECTIONSTATUS IPX |                         | x                   | x          | x            | x           | x             |
| \_STOPFILTERPTYPE IPX        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

As opções de soquete **\_ IPX NSPROTO** a seguir foram definidas no Windows sockets 2 Protocol-Specific anexo, mas não são implementadas pelo protocolo IPX/SPX do Windows.

*nível* **=** do **NSPROTO \_ IPX**



| Opção           | Type | Padrão                         | Significado                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_soma de verificação IPX    | Bool | Desligar                             | Quando definido, o IPX executa uma soma de verificação em pacotes de saída e verifica a soma de verificação de pacotes de entrada.                                                          |
| \_TXPKTSIZE IPX   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagrama de envio. Esse tamanho não inclui o cabeçalho IPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia.    |
| \_RXPKTSIZE IPX   | INT  | Tamanho da mídia para um máximo de 1466 | Define o tamanho máximo de datagramas de recebimento. Esse tamanho não inclui o cabeçalho IPX ou todos os cabeçalhos de mídia que também podem ser usados. Pode ser aumentado para o tamanho da mídia. |
| \_TXMEDIASIZE IPX | INT  | Placa principal                   | Retorna o tamanho da mídia de envio que define um limite superior para o tamanho do datagrama.                                                                                       |
| \_RXMEDIASIZE IPX | INT  | Placa principal                   | Retorna o tamanho da mídia de recebimento que define um limite superior para o tamanho do datagrama.                                                                                    |
| IPX \_ primário     | Bool | Primário                         | Restringe o tráfego para a placa de rede primária.                                                                                                               |



 

As opções de soquete **NSPROTO \_ SPX** a seguir foram definidas no Windows sockets 2 Protocol-Specific anexo, mas não são implementadas no Windows pelo protocolo IPX/SPX do Windows.

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



 

 




