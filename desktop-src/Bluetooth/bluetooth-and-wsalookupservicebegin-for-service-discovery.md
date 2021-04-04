---
title: Bluetooth e WSALookupServiceBegin para descoberta de serviço
description: Para descobrir a existência de um serviço específico em um servidor Bluetooth, os clientes usam as funções WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth e WSALookupServiceBegin para o Bluetooth de descoberta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824038"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth e WSALookupServiceBegin para descoberta de serviço

Para descobrir a existência de um serviço específico em um servidor Bluetooth, os clientes usam as funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) . As consultas podem ser executadas para endereços locais e remotos, mas as conexões só podem ser estabelecidas com endereços remotos. Os identificadores de serviço descobertos durante essa operação não podem ser usados para excluir o serviço por meio de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea). O loopback não tem suporte do RFCOMM.

Dois tipos básicos de consultas de descoberta de serviço podem ser executados:

-   Consultas para um ou mais serviços no dispositivo local
-   Consultas para um ou mais serviços em um dispositivo de mesmo nível especificado

A função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) recebe uma estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) em seu parâmetro *lpqsRestrictions* . **WSALookupServiceBegin** executa uma consulta de cliente com base no conjunto de restrições de pesquisa que o **WSAQUERYSET** contém. Os clientes Bluetooth devem especificar as restrições, listadas na tabela a seguir, na estrutura **WSAQUERYSET** ao usar a função **WSALookupServiceBegin** para consultar serviços.



| Membro WSAQUERYSET    | Restrição                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Defina como **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Defina como o UUID Bluetooth mais específico que pode ser usado para determinar o escopo da consulta. Por exemplo, a configuração de **lpServiceClassId** para o UUID do protocolo L2CAP resulta em todos os serviços L2CAP retornados, basicamente enumerando todos os registros SD no destino. No entanto, definir o UUID para um serviço específico retorna apenas as instâncias desse serviço.<br/> |
| **dwNameSpace**       | Defina como **ns \_ BTH**.                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Defina como 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Defina para o endereço de dispositivo Bluetooth com o qual estabelecer uma conexão SDP para executar a consulta de serviços. Esse membro deve ser uma cadeia de caracteres que é convertida usando a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Se o endereço de rádio local for fornecido, os registros SDP locais serão pesquisados.<br/>                                             |
| Outros membros         | Todos os outros membros da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) são ignorados.                                                                                                                                                                                                                                                                                        |



 

A conexão SDP com o dispositivo remoto não permanece ativa após a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) concluir uma consulta de serviço; a conexão é encerrada antes de o **WSALookupServiceBegin** retornar. Os aplicativos que exigem a conexão SDP permanecerão ativas após a conclusão de uma consulta de serviço devem especificar o UUID de classe de serviço ao qual se conectar usando o membro Service **ClassID** da estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) ao emitir a chamada de função do Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

Os sinalizadores, listados na tabela a seguir, são usados no parâmetro *dwControlFlags* das funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para controlar os resultados da consulta. Os **\_ contêineres Lup** e sinalizadores **Lup \_ FLUSHCACHE** são usados pela função **WSALookupServiceBegin** ; o restante dos sinalizadores é usado em chamadas para a função **WSALookupServiceNext** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sinalizador</th>
<th>Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>Não deve ser definido.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>Os aplicativos geralmente devem especificar <strong>LUP_FLUSHCACHE</strong>. Esse sinalizador instrui o sistema a ignorar todas as informações armazenadas em cache e estabelecer uma conexão SDP over-the-Air para o dispositivo especificado para executar a pesquisa SDP. Essa operação não armazenada em cache pode levar vários segundos (enquanto uma pesquisa armazenada em cache retorna rapidamente). No momento, o Bluetooth não armazena de forma proativa os registros SDP de dispositivos próximos, nem atualmente faz o cache de consultas anteriores no momento. Portanto, os aplicativos devem prever que as consultas podem não retornar resultados (com um código de erro de <strong>WSASERVICE_NOT_FOUND</strong>) se <strong>LUP_FLUSHCACHE</strong> não for especificado. Os dados armazenados em cache que estão disponíveis usando a interface do Windows Sockets podem ser aprimorados no futuro.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Retornar informações sobre o endereço Bluetooth local. Esse sinalizador terá efeito somente se <strong>LUP_RETURN_ADDR</strong> também for especificado.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Retorne o nome de exibição do serviço no membro <strong>lpszServiceInstanceName</strong> da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada chamada para a função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Retorne a ID de classe de serviço no membro <strong>lpServiceClassId</strong> da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .
<blockquote>
[!Note]<br />
O uso desse sinalizador só é aplicável à função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>WSALookupServiceBegin</strong></a> . Esse valor é sempre zero para <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Retorne um endereço no membro <strong>lpcsaBuffer</strong> para ser usado com chamadas de função de <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>conexão</strong></a> . O endereço retornado contém o número da porta.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Retorne os registros SD correspondentes no membro <strong>lpBlob</strong> , formatados de acordo com a especificação de registro SDP do Bluetooth.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Retornar todas as informações sobre os sinalizadores acima.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Retorne a descrição do serviço no membro <strong>lpszComment</strong> da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada chamada para a função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Ignore o próximo registro disponível e retorne o registro que o segue.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Consultas de serviço avançadas

As operações de consulta descritas na seção anterior podem ser usadas para retornar todos os resultados de um único GUID, o que deve ser suficiente para a maioria dos aplicativos. Uma consulta avançada permite que um aplicativo crie uma consulta mais específica; Ele fornece a capacidade de corresponder UUIDs e atributos nas informações retornadas.

Para executar uma consulta avançada para serviços, os clientes Bluetooth devem especificar as seguintes restrições na estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que é passada para o parâmetro *lpqsRestrictions* .



| Membro WSAQUERYSET   | Restrição                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Defina como **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Defina para o endereço de dispositivo Bluetooth com o qual estabelecer uma conexão SDP para executar a consulta de serviços. Esse membro deve ser uma cadeia de caracteres que é convertida usando a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Se o endereço de rádio local for fornecido, os registros SDP locais serão pesquisados.<br/> |
| **lpBlob.pBlobData** | Ponteiro para uma estrutura de [**\_ \_ serviço de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contém todos os parâmetros que limitam os resultados da consulta.                                                                                                                                                                                           |
| **dwNameSpace**      | Defina como **ns \_ BTH**.                                                                                                                                                                                                                                                                                                                 |
| Outros membros        | Todos os outros membros da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) são ignorados.                                                                                                                                                                                                                                            |



 

Os sinalizadores a seguir são passados no parâmetro *dwControlFlags* de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para controlar os resultados de uma consulta avançada.

| Sinalizador                     | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_contêineres de Lup**      | Não deve ser definido.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | Os aplicativos geralmente devem especificar **Lup \_ FLUSHCACHE**. Esse sinalizador instrui o sistema a ignorar todas as informações armazenadas em cache e estabelecer uma conexão SDP over-the-Air para o dispositivo especificado para executar a pesquisa SDP. Essa operação não armazenada em cache pode levar vários segundos (enquanto uma pesquisa armazenada em cache retorna rapidamente). O Bluetooth não armazena de forma proativa os registros SDP de dispositivos próximos, nem armazena agressivamente as consultas anteriores em cache. Portanto, os aplicativos devem esperar que as consultas com frequência não retornem nenhum resultado (**WSASERVICE \_ não \_ encontrado**) se **Lup \_ FLUSHCACHE** não for especificado. Os dados armazenados em cache que estão disponíveis usando a interface do Windows Sockets podem ser aprimorados no futuro. |
| **\_serviço Lup res \_**    | Retornar informações para o endereço local do Bluetooth. A definição desse sinalizador terá efeito somente se o **Lup de \_ retorno do remetente \_** também for especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **LUP \_ nome de retorno \_**    | Retornar o nome de exibição do serviço. Esse sinalizador é ignorado para **a \_ \_ \_ solicitação de pesquisa do serviço SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_tipo de retorno Lup \_**    | Retornar a ID de classe de serviço. Esse sinalizador é ignorado para **a \_ \_ \_ solicitação de pesquisa do serviço SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_endereço de retorno de Lup \_**    | Retorne um endereço no membro **lpcsaBuffer** para ser usado com chamadas de função de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) . O endereço retornado contém o número da porta. Esse sinalizador é ignorado para **a \_ \_ \_ solicitação de pesquisa do serviço SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **\_blob de retorno de Lup \_**    | Retorne os registros SD correspondentes em um formato que esteja de acordo com a especificação de registro SDP do Bluetooth. Para **a \_ \_ \_ solicitação de pesquisa de serviço SDP**, o resultado em **LpBlob** para a chamada subsequente para [**WSALOOKUPSERVICENEXT**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) é uma matriz de identificadores de SDP de Bluetooth. Para solicitação de **\_ \_ atributo \_ de serviço SDP** e **solicitação de atributo de \_ pesquisa de serviço \_ \_ \_ SDP**, o resultado de cada chamada subsequente para **WSALookupServiceNext** é um registro de SDP Bluetooth binário cujos atributos são restritos àqueles especificados pelo membro **pRange** da consulta. Esse sinalizador é necessário para **a \_ \_ \_ solicitação de pesquisa de serviço SDP**.                                                               |
| **\_Comentário de retorno do Lup \_** | Retorne a descrição do serviço no membro **lpszComment** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | Ignore o próximo registro disponível e retorne o registro que o segue.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

Na entrada, **lpBlob** -> **pBlobData** aponta para uma estrutura de [**\_ \_ serviço de consulta do BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contém os valores listados na tabela a seguir.

> [!Note]  
> A solicitação inicial de pesquisa deve ser capaz de se ajustar a um pacote L2CAP. A resposta, no entanto, pode ser dividida em vários pacotes L2CAP.

 



| Membro            | Valor                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tipo**          | Tipo de pesquisa a ser executada. Esse valor pode ser uma das solicitações de **\_ \_ pesquisa \_ de serviço SDP**, **solicitação de \_ atributo de serviço \_ \_ SDP** ou solicitação de atributo de **pesquisa de \_ serviço \_ \_ \_ SDP**. Cada tipo de pesquisa é associado a um mecanismo de pesquisa subjacente que é definido pela especificação de SDP do Bluetooth. Cada retorno resulta no formulário descrito pela estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que é definida anteriormente nesta seção (consultas de serviço avançadas). |
| **Gerenciador de controle** | Usado para pesquisas de atributo. Esse valor especifica o identificador de serviço com o qual consultar os atributos no membro **pRange** .                                                                                                                                                                                                                                                                                                                                            |
| **UUIDs**         | Usado para pesquisas de serviço e **ServiceAttribute** . Esse valor especifica os UUIDs que um registro deve conter para corresponder à pesquisa. Se for necessário consultar os UUIDs inferiores a Max nos UUIDs de **\_ \_ \_ consulta** , esse valor definirá o elemento SdpQueryUuid que segue imediatamente o último UUID válido para todos os zeros.                                                                                                                                                                       |
| **numRange**      | Usado para pesquisas de atributo e **ServiceAttribute** . Esse valor especifica o número de elementos em **pRange**.                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | Usado para pesquisas de atributo e **ServiceAttribute** . Esse valor especifica os valores de atributo a serem recuperados para qualquer registro correspondente.                                                                                                                                                                                                                                                                                                                                        |



 

Após cada chamada bem-sucedida para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , **lpBlob** -> **pBlobData** aponta para um bloco de dados que contém os valores listados na tabela a seguir.

| Valor                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_solicitação de \_ pesquisa do serviço SDP \_**                                                    | Uma matriz de identificadores de registro SDP que é idêntica à **ServiceRecordHandleList** definida pelo Bluetooth 1,1 SDP 4.5.2. O número de identificadores SDP que é retornado é calculado por (**lpBlob**->cbSize)/**sizeof**(ULong). Todos os resultados são retornados em uma única chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . |
| **SDP \_ Solicitação \_ de \_** atributo de serviço ou **solicitações de atributo de \_ pesquisa de serviço \_ \_ \_ SDP** | Um registro de SDP Bluetooth binário. Para **a \_ \_ \_ solicitação de atributo de serviço SDP**, todos os resultados são retornados em uma única chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                       |



 

> [!Note]  
> Se o membro **lpBlob** não for especificado durante a entrada de uma consulta de serviço, uma pesquisa de serviço e de atributo será executada para o serviço especificado no membro **lpServiceClassId** em atributos de 0 a 0xFFFF.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSAQUERYSET para consulta de serviço](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Descobrir dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**\_serviço de consulta do BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

