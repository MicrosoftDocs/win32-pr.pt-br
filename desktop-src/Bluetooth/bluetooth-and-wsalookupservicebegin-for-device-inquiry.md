---
title: Bluetooth e WSALookupServiceBegin para consulta de dispositivo
description: Este tópico descreve como usar a função WSALookupServiceBegin para executar uma consulta de dispositivos visíveis e fantasmas. Para obter mais informações, consulte descobrindo dispositivos e serviços Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin para consulta de dispositivo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084960"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth e WSALookupServiceBegin para consulta de dispositivo

Este tópico descreve como usar a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para executar uma consulta de dispositivos visíveis e fantasmas. Para obter mais informações, consulte [descobrindo dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md).

A função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) em seu primeiro parâmetro, *lpqsRestrictions*, para definir critérios de pesquisa. O Bluetooth fornece diretrizes específicas para o uso da função **WSALookupServiceBegin** e do **WSAQUERYSET**.

A tabela a seguir lista as restrições que se aplicam à estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passada para o parâmetro *lpqsRestrictions* ao consultar dispositivos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro WSAQUERYSET</th>
<th>Restrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Defina como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>Esse membro contém um ponteiro opcional para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> . Se esse membro for especificado, os parâmetros de consulta do dispositivo válidos para <strong>LUP_FLUSHCACHE</strong> serão os seguintes:
<ul>
<li>O membro <strong>cbSize</strong> da estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> deve ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li>
<li>O membro <strong>pBlobData</strong> é um ponteiro para uma estrutura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , para o qual o membro de <strong>LAP</strong> é o código de acesso de consulta Bluetooth, e <strong>o comprimento do membro é</strong> o comprimento, em segundos, da consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Defina como <strong>NS_BTH</strong>.</td>
</tr>
<tr class="even">
<td>Outros membros</td>
<td>Outros membros da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> são ignorados.</td>
</tr>
</tbody>
</table>



 

Os sinalizadores listados na tabela a seguir são usados no parâmetro *dwControlFlags* para controlar os resultados da consulta. Os **\_ contêineres Lup** e sinalizadores **Lup \_ FLUSHCACHE** são usados pela função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; o restante dos sinalizadores é usado em chamadas para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Sinalizador               | Resultado                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_contêineres de Lup    | Especifica que a finalidade da consulta é obter uma lista de dispositivos Bluetooth e não uma lista de serviços. Esse sinalizador deve ser definido.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Dispara uma consulta de dispositivos locais ou faz com que os resultados em cache de consultas anteriores sejam retornados.                                                                                                                                                                                                                                                                                                                |
| \_tipo de retorno Lup \_  | Retorne o Bluetooth COD (classe de bits de dispositivo) diretamente no membro **lpServiceClassId** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . O COD é mapeado para o membro **dados1** do GUID.                                                                                                                                                                                                      |
| \_serviço Lup res \_  | Retornar informações para o endereço local do Bluetooth. Esse sinalizador terá efeito somente se o **\_ \_ endereço de retorno de Lup** também for especificado.                                                                                                                                                                                                                                                                                       |
| LUP \_ nome de retorno \_  | Retorne o nome de exibição do dispositivo no membro **lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Esse sinalizador também deve ser especificado para recuperar o **nome** membro da estrutura [**de \_ \_ informações do dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) ao especificar o sinalizador de **retorno de \_ \_ blob Lup** . |
| \_endereço de retorno de Lup \_  | Retorne uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contém o endereço de 48 bits do par no membro **lpcsaBuffer** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Outros membros na estrutura **SOCKADDR \_ BTH** estarão vazios.                                                            |
| \_blob de retorno de Lup \_  | Retorne a estrutura de [**\_ \_ informações do dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) em cada chamada subsequente para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Ignore o próximo dispositivo disponível e retorne o dispositivo que o segue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Descobrir dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo de consulta BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 