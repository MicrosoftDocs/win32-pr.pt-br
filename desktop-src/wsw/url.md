---
title: Url
description: Os elementos da API da URL do WWSAPI fornecem mecanismos para dividir e cancelar a saída de URLs em partes de componente e para escapar e combinar partes de componentes de volta em uma URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Serviços Web de URL para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8048a2e6e3e222de82234769813cead3ee7eb362c51355a1b516396de2c6d58b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119325296"
---
# <a name="url"></a>Url

Os elementos da API da URL do WWSAPI fornecem mecanismos para dividir e cancelar a saída de URLs em partes de componente e para escapar e combinar partes de componentes de volta em uma URL.

-   Para dividir e cancelar a saída de URLs em partes de componente, use a função [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .
-   Para escapar e combinar partes componentes de volta em uma URL, use a função [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .
-   Para combinar URLs relativas com uma URL base absoluta formando uma URL absoluta, use a função [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .

As seguintes enumerações fazem parte da URL:

-   [**\_sinalizadores de URL do WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo de \_ esquema de URL do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

As funções a seguir fazem parte da URL:

-   [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

As seguintes estruturas fazem parte da URL:

-   [**\_URL WS https \_**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**\_URL http do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**\_URL do NETPIPE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**URL do WS \_ NETTCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**URL do WS \_ SOAPUDP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**URL do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




