---
title: Bluetooth e WSAQUERYSET para consulta de serviço
description: Usando a estrutura WSAQUERYSET com as funções WSALookupServiceBegin e WSALookupServiceNext para obter informações sobre o processo de consulta de serviço.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET para consulta de serviço Bluetooth
- WSAQUERYSET Bluetooth, para consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642325"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET para consulta de serviço

O Bluetooth usa a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , com várias funções, para facilitar a descoberta de dispositivos e serviços no namespace do Bluetooth, NS \_ BTH.

As funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usam a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obter dados sobre o processo de consulta de serviço. A tabela a seguir descreve como definir os valores de membro na estrutura **WSAQUERYSET** para essa finalidade.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>Entrada para WSALookupServiceBegin</th>
<th>Valor retornado de WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Deve ser definido como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retornado pelo sistema.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>Não usado.</td>
<td>Nome de exibição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP do ServiceName do Bluetooth. Retornado se LUP_RETURN_NAME for especificado.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obrigatórios. O UUID de Bluetooth único mais específico para os serviços para os quais a pesquisa está sendo realizada. Por exemplo, se esse valor for definido como o UUID do protocolo L2CAP, ele retornará todos os serviços usando o protocolo L2CAP no dispositivo de destino. Se definido como o UUID de um serviço específico, ele retornará apenas as instâncias desse serviço.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>Não usado.</td>
<td>Descrição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP ServiceDescription do Bluetooth. Retornado se <strong>LUP_RETURN_COMMENT</strong> for especificado.</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Deve ser NS_BTH.</td>
<td>Retorna NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>lpszContext</strong></td>
<td>Obrigatórios. O endereço do dispositivo Bluetooth com o qual estabelecer uma conexão SDP e consultar serviços. Esse valor deve ser uma cadeia de caracteres que foi convertida usando a chamada de função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . Se o endereço do dispositivo Bluetooth local for fornecido, o banco de dados SDP local será pesquisado.</td>
<td>Não usado.</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>Não usado.</td>
<td>Indica o número de elementos na matriz de estruturas de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>Não usado.</td>
<td>Ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cujo membro <strong>localaddr. lpSockAddr</strong> aponta para uma <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contém o endereço de conexão completo do serviço remoto, convertido da primeira entrada do atributo de SDP de ProtocolDescriptorList do Bluetooth. Retornado se <strong>LUP_RETURN_ADDR</strong> for especificado.</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>Opcional. Ponteiro para uma estrutura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contém parâmetros avançados para limitar os resultados da pesquisa. Se fornecido, <strong>lpServiceClassId</strong> será ignorado e as consultas em cache não serão executadas com sucesso.</td>
<td><ul>
<li>Se uma pesquisa de serviço for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna os identificadores de serviço. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULong) calcula o número de identificadores. <strong>BLOB. pBlobData</strong> é uma matriz de valores ULONG que representa os identificadores de serviço.</li>
<li>Se uma pesquisa de atributo ou ServiceAttribute for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna o registro SDP binário. <strong>BLOB. cbSize</strong> é o tamanho do registro SDP binário. <strong>BLOB. pBlobData</strong> aponta para o próprio registro. O registro de SDP binário é necessário em muitos casos porque apenas um número limitado de atributos SDP pode ser convertido na estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e somente as cadeias de caracteres UTF-8 codificadas por padrão são convertidas. As funções para auxiliar na análise do registro SDP binário são fornecidas na seção de <a href="bluetooth-reference.md">referência do Bluetooth</a> .</li>
<li>Retornado se LUP_RETURN_BLOB for especificado.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSAQUERYSET para o serviço set](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Referência de Bluetooth](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_serviço de consulta do BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**informações de CSADDR \_**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 