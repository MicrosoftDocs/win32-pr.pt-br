---
title: Bluetooth e WSAQUERYSET para consulta de serviço
description: Usando a estrutura WSAQUERYSET com as funções WSALookupServiceBegin e WSALookupServiceNext para obter informações sobre o processo de consulta de serviço.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth Bluetooth e WSAQUERYSET para consulta de serviço
- WSAQUERYSET Bluetooth, para consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467093"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth e WSAQUERYSET para consulta de serviço

Bluetooth usa a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , com várias funções, para facilitar a descoberta de dispositivos e serviços no namespace Bluetooth, NS \_ BTH.

As funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usam a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obter dados sobre o processo de consulta de serviço. A tabela a seguir descreve como definir os valores de membro na estrutura **WSAQUERYSET** para essa finalidade.




| Membro | Entrada para WSALookupServiceBegin | Valor retornado de WSALookupServiceNext | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize</strong> | Deve ser definido como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retornado pelo sistema. | 
| <strong>dwOutputFlags</strong> | Não usado. | Não usado. | 
| <strong>lpszServiceInstanceName</strong> | Não usado. | nome de exibição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP do Bluetooth servicename. Retornado se LUP_RETURN_NAME for especificado. | 
| <strong>lpServiceClassId</strong> | Obrigatórios. o UUID de Bluetooth único mais específico para os serviços para os quais a pesquisa está sendo realizada. Por exemplo, se esse valor for definido como o UUID do protocolo L2CAP, ele retornará todos os serviços usando o protocolo L2CAP no dispositivo de destino. Se definido como o UUID de um serviço específico, ele retornará apenas as instâncias desse serviço. | Não usado. | 
| <strong>lpVersion</strong> | Não usado. | Não usado. | 
| <strong>lpszComment</strong> | Não usado. | descrição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP do Bluetooth servicedescription. Retornado se <strong>LUP_RETURN_COMMENT</strong> for especificado. | 
| <strong>dwNameSpace</strong> | Deve ser NS_BTH. | Retorna NS_BTH. | 
| <strong>lpNSProviderId</strong> | Não usado. | Não usado. | 
| <strong>lpszContext</strong> | Obrigatórios. o endereço de dispositivo Bluetooth com o qual estabelecer uma conexão SDP e consultar serviços. Esse valor deve ser uma cadeia de caracteres que foi convertida usando a chamada de função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . se o endereço do dispositivo Bluetooth local for fornecido, o banco de dados SDP local será pesquisado. | Não usado. | 
| <strong>dwNumberOfProtocols</strong> | Não usado. | Não usado. | 
| <strong>lpafpProtocols</strong> | Não usado. | Não usado. | 
| <strong>lpszQueryString</strong> | Não usado. | Não usado. | 
| <strong>dwNumberOfCsAddrs</strong> | Não usado. | Indica o número de elementos na matriz de estruturas de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> . | 
| <strong>lpcsaBuffer</strong> | Não usado. | ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cujo membro <strong>LocalAddr. lpSockaddr</strong> aponta para uma <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contém o endereço de conexão completo do serviço remoto, convertido da primeira entrada do atributo Bluetooth ProtocolDescriptorList SDP. Retornado se <strong>LUP_RETURN_ADDR</strong> for especificado. | 
| <strong>lpBlob</strong> | Opcional. Ponteiro para uma estrutura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contém parâmetros avançados para limitar os resultados da pesquisa. Se fornecido, <strong>lpServiceClassId</strong> será ignorado e as consultas em cache não serão executadas com sucesso. | <ul><li>Se uma pesquisa de serviço for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna os identificadores de serviço. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULong) calcula o número de identificadores. <strong>BLOB. pBlobData</strong> é uma matriz de valores ULONG que representa os identificadores de serviço.</li><li>Se uma pesquisa de atributo ou ServiceAttribute for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna o registro SDP binário. <strong>BLOB. cbSize</strong> é o tamanho do registro SDP binário. <strong>BLOB. pBlobData</strong> aponta para o próprio registro. O registro de SDP binário é necessário em muitos casos porque apenas um número limitado de atributos SDP pode ser convertido na estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e somente as cadeias de caracteres UTF-8 codificadas por padrão são convertidas. as funções para auxiliar na análise do registro SDP binário são fornecidas na seção <a href="bluetooth-reference.md">referência de Bluetooth</a> .</li><li>Retornado se LUP_RETURN_BLOB for especificado.</li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSAQUERYSET para o serviço de conjunto](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para a consulta do dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth e WSALookupServiceNext
</dt> <dt>

[Bluetooth Referência](bluetooth-reference.md)
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

 

 
