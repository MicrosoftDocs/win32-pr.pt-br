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
# <a name="supported-certificate-formats"></a><span data-ttu-id="342fc-103">Formatos de certificado com suporte</span><span class="sxs-lookup"><span data-stu-id="342fc-103">Supported Certificate Formats</span></span>

<span data-ttu-id="342fc-104">Os serviços de certificados podem emitir os seguintes tipos de certificados.</span><span class="sxs-lookup"><span data-stu-id="342fc-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="342fc-105">Termo</span><span class="sxs-lookup"><span data-stu-id="342fc-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="342fc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="342fc-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="342fc-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticação de cliente compatível com SSL do [*X. 509*](../secgloss/x-gly.md) versão 3</span><span class="sxs-lookup"><span data-stu-id="342fc-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="342fc-108">Esse certificado de autenticação de cliente identifica um cliente e é usado por servidores para autenticar um cliente que solicita acesso ao servidor.</span><span class="sxs-lookup"><span data-stu-id="342fc-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="342fc-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticação de servidor compatível com SSL X. 509 v3</span><span class="sxs-lookup"><span data-stu-id="342fc-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="342fc-110">Esse certificado de autenticação de servidor identifica um servidor e é usado pelos clientes para autenticar um servidor que o cliente deseja acessar.</span><span class="sxs-lookup"><span data-stu-id="342fc-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="342fc-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificado [*S/MIME*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="342fc-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="342fc-112">Esse certificado é usado por clientes para email seguro no protocolo S/MIME (Secure/Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="342fc-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="342fc-113">Além desses certificados, os serviços de certificados também podem ser usados para emitir outros certificados X. 509 escrevendo um módulo de política personalizado.</span><span class="sxs-lookup"><span data-stu-id="342fc-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="342fc-114">"Certificado de autenticação de servidor" e "certificado de servidor", bem como "certificado de autenticação de cliente" e "certificado de cliente" são termos intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="342fc-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="342fc-115">Além disso, os serviços de certificados incluem modelos de certificado na configuração da autoridade de certificação corporativa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="342fc-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="342fc-116">Consulte a documentação de ajuda do Windows para modelos de certificado para entender como eles definem as finalidades de certificado.</span><span class="sxs-lookup"><span data-stu-id="342fc-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
