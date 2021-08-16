---
title: Bluetooth e WSAQUERYSET para consulta de serviço
description: Usando a estrutura WSAQUERYSET com as funções WSALookupServiceBegin e WSALookupServiceNext para obter informações sobre o processo de consulta de serviço.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET para consulta de serviço Bluetooth
- WSAQUERYSET Bluetooth , para consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959155"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET para consulta de serviço

Bluetooth usa a estrutura [**WSAQUERYSET,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) com várias funções, para facilitar a descoberta de dispositivos e serviços no namespace Bluetooth, NS \_ BTH.

As [**funções WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usam a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obter dados sobre o processo de consulta de serviço. A tabela a seguir descreve como definir os valores de membro na estrutura **WSAQUERYSET** para essa finalidade.



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
<td><strong>Dwsize</strong></td>
<td>Deve ser definido como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retornado pelo sistema.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>Não usado.</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td><strong>Lpszserviceinstancename</strong></td>
<td>Não usado.</td>
<td>Nome de exibição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP Bluetooth ServiceName. Retornado se LUP_RETURN_NAME for especificado.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obrigatórios. O único UUID Bluetooth mais específico para os serviços para os quais a pesquisa está sendo realizada. Por exemplo, se esse valor for definido como o UUID do protocolo L2CAP, ele retornará todos os serviços usando o protocolo L2CAP no dispositivo de destino. Se definido como o UUID de um serviço específico, ele retornará apenas as instâncias desse serviço.</td>
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
<td>Descrição do serviço, convertida como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP Bluetooth ServiceDescription. Retornado se <strong>LUP_RETURN_COMMENT</strong> for especificado.</td>
</tr>
<tr class="odd">
<td><strong>Dwnamespace</strong></td>
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
<td>Obrigatórios. O Bluetooth de dispositivo com o qual estabelecer uma conexão SDP e consultar serviços. Esse valor deve ser uma cadeia de caracteres que foi convertida usando a chamada de função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString.</strong></a> Se o endereço Bluetooth do dispositivo local for fornecido, o banco de dados SDP local será pesquisado.</td>
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
<td>Indica o número de elementos na matriz de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> estruturas.</td>
</tr>
<tr class="even">
<td><strong>Lpcsabuffer</strong></td>
<td>Não usado.</td>
<td>Ponteiro para uma <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>estrutura CSADDR_INFO</strong></a> cujo membro <strong>LocalAddr.lpSockaddr</strong> aponta para um <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contém o endereço conectável completo do serviço remoto, convertido da primeira entrada do atributo SDP protocolDescriptorList do Bluetooth. Retornado se <strong>LUP_RETURN_ADDR</strong> for especificado.</td>
</tr>
<tr class="odd">
<td><strong>Lpblob</strong></td>
<td>Opcional. Ponteiro para uma <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contém parâmetros avançados para limitar os resultados da pesquisa. Se fornecido, <strong>lpServiceClassId</strong> será ignorado e as consultas armazenadas em cache não são bem-sucedidas.</td>
<td><ul>
<li>Se uma pesquisa de serviço for executada: ponteiro para uma estrutura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que retorna as alças de serviço. (<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcula o número de alças. <strong>BLOB.pBlobData é</strong> uma matriz de valores ULONG que representam os alças de serviço.</li>
<li>Se uma pesquisa de atributo ou serviceAttribute for executada: ponteiro para uma estrutura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que retorna o registro SDP binário. <strong>BLOB.cbSize</strong> é o tamanho do registro SDP binário. <strong>BLOB.pBlobData</strong> aponta para o próprio registro. O registro SDP binário é necessário em muitos casos porque apenas um número limitado de atributos SDP podem ser convertidos na estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e apenas cadeias de caracteres UTF-8 codificadas padrão são convertidas. As funções para ajudar na análise do registro SDP binário são fornecidas na <a href="bluetooth-reference.md">seção referência Bluetooth</a> dados.</li>
<li>Retornado se LUP_RETURN_BLOB for especificado.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSAQUERYSET para Definir Serviço](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Bluetooth Referência](bluetooth-reference.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**SERVIÇO \_ DE CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**INFORMAÇÕES DO \_ CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 