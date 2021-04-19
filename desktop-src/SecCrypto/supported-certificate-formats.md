---
description: Lista os formatos de certificado com suporte nos serviços de certificados.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formatos de certificado com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780463"
---
# <a name="supported-certificate-formats"></a>Formatos de certificado com suporte

Os serviços de certificados podem emitir os seguintes tipos de certificados.



| Termo                                                                                                                                                                                                                                                                                                                                                                                             | Descrição                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticação de cliente compatível com SSL do [*X. 509*](../secgloss/x-gly.md) versão 3<br/> | Esse certificado de autenticação de cliente identifica um cliente e é usado por servidores para autenticar um cliente que solicita acesso ao servidor.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticação de servidor compatível com SSL X. 509 v3<br/>                                                                                         | Esse certificado de autenticação de servidor identifica um servidor e é usado pelos clientes para autenticar um servidor que o cliente deseja acessar.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificado [*S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Esse certificado é usado por clientes para email seguro no protocolo S/MIME (Secure/Multipurpose Internet Mail Extensions).<br/>              |



 

Além desses certificados, os serviços de certificados também podem ser usados para emitir outros certificados X. 509 escrevendo um módulo de política personalizado.

> [!Note]  
> "Certificado de autenticação de servidor" e "certificado de servidor", bem como "certificado de autenticação de cliente" e "certificado de cliente" são termos intercambiáveis.

 

Além disso, os serviços de certificados incluem modelos de certificado na configuração da autoridade de certificação corporativa da Microsoft. Consulte a documentação de ajuda do Windows para modelos de certificado para entender como eles definem as finalidades de certificado.

 

 
