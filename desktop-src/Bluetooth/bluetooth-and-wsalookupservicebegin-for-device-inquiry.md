---
title: Bluetooth e WSALookupServiceBegin para consulta de dispositivo
description: Este tópico descreve como usar a função WSALookupServiceBegin para executar uma consulta de dispositivos visíveis e fantasmas. Para obter mais informações, consulte Descoberta Bluetooth dispositivos e serviços.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin para consulta de dispositivo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4423b7c1c27124771c518409d9d1393a5f83afb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469183"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth e WSALookupServiceBegin para consulta de dispositivo

Este tópico descreve como usar a [**função WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para executar uma consulta de dispositivos visíveis e fantasmas. Para obter mais informações, consulte [Descoberta de Bluetooth dispositivos e serviços](discovering-bluetooth-devices-and-services.md).

A [**função WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) em seu primeiro parâmetro, *lpqsRestrictions*, para definir critérios de pesquisa. Bluetooth fornece diretrizes específicas para uso da **função WSALookupServiceBegin** e **WSAQUERYSET**.

A tabela a seguir lista as restrições que se aplicam à estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passada para o parâmetro *lpqsRestrictions* ao consultar dispositivos.




| Membro WSAQUERYSET | Restrição | 
|--------------------|-------------|
| <strong>Dwsize</strong> | Definido como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | 
| <strong>Lpblob</strong> | Esse membro contém um ponteiro opcional para uma estrutura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB.</strong></a> Se esse membro for especificado, os parâmetros de consulta de dispositivo válidos <strong>para</strong> LUP_FLUSHCACHE serão os exemplos a seguir:<ul><li>O <strong>membro cbSize</strong> da estrutura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> deve ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li><li>O <strong>membro pBlobData</strong> é um ponteiro para uma estrutura <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE,</strong></a> para a qual o membro <strong></strong> <strong>LAP</strong> é o código de acesso de consulta Bluetooth e o membro de comprimento é o comprimento, em segundos, da consulta.</li></ul> | 
| <strong>Dwnamespace</strong> | Definido como <strong>NS_BTH</strong>. | 
| Outros membros | Outros membros da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> são ignorados. | 




 

Os sinalizadores listados na tabela a seguir são usados no *parâmetro dwControlFlags* para controlar os resultados da consulta. Os **sinalizadores LUP \_ CONTAINERS** e **LUP \_ FLUSHCACHE** são usados pela função [**WSALookupServiceBegin;**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o restante dos sinalizadores é usado em chamadas para a [**função WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)

| Sinalizador               | Resultado                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTÊINERES LUP \_    | Especifica que a finalidade da consulta é obter uma lista de Bluetooth e não uma lista de serviços. Esse sinalizador deve ser definido.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Dispara uma consulta de dispositivos locais ou faz com que os resultados armazenados em cache de consultas anteriores sejam retornados.                                                                                                                                                                                                                                                                                                                |
| TIPO DE \_ RETORNO \_ LUP  | Retorne o Bluetooth COD (classe de bits de dispositivo) diretamente no membro **lpServiceClassId** da [**estrutura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) O COD é mapeado para **o membro Data1** do GUID.                                                                                                                                                                                                      |
| LUP \_ RES \_ SERVICE  | Retornar informações para o endereço Bluetooth local. Esse sinalizador só terá efeito se **LUP \_ RETURN \_ ADDR** também for especificado.                                                                                                                                                                                                                                                                                       |
| LUP \_ RETURN \_ NAME  | Retorne o nome de exibição do dispositivo no membro **lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a [**função WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Esse sinalizador também deve ser especificado para recuperar o membro **de** nome da estrutura [**BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) ao especificar o **sinalizador LUP RETURN \_ \_ BLOB.** |
| LUP \_ RETURN \_ ADDR  | Retornar [**uma estrutura \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contém o endereço de 48 bits do par no membro **lpcsaBuffer** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a [**função WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Outros membros na estrutura **SOCKADDR \_ BTH** estarão vazios.                                                            |
| LUP \_ RETURN \_ BLOB  | Retorne a [**estrutura BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) em cada chamada subsequente para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Ignore o próximo dispositivo disponível e retorne o dispositivo que o segue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSALookupServiceBegin para Descoberta de Serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Descobrir dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**Wsalookupservicenext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**Wsalookupserviceend**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**DISPOSITIVO DE \_ CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
