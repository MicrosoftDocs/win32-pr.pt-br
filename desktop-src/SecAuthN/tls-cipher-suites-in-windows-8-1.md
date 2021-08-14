---
description: Conjuntos de codificação TLS no Windows 8.1
ms.assetid: 48A515C2-96D3-4CBF-A48F-3F0B91F0CB2C
title: Conjuntos de codificação TLS no Windows 8.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316dc649379f785662d1d818d0af11d882c33f1236113a0c8a8f71458b7e964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916125"
---
# <a name="tls-cipher-suites-in-windows-81"></a>Conjuntos de codificação TLS no Windows 8.1

Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles. A versão mais alta com suporte do TLS é sempre preferida no handshake de TLS. Por exemplo, SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5 só pode ser usado quando o cliente e o servidor não dão suporte a TLS 1,2, 1,1 & 1,0 ou SSL 3,0, pois ele só tem suporte com SSL 2,0.

A disponibilidade de conjuntos de codificação deve ser controlada de uma das duas maneiras:

-   A ordem de prioridade padrão é substituída quando uma lista de prioridades é configurada. Os conjuntos de codificação que não estão na lista de prioridades não serão usados.
-   Permitido quando o aplicativo passa \_ SCH \_ usar \_ criptografia forte: o provedor Microsoft Schannel filtrará pacotes de criptografia fracos conhecidos quando o aplicativo usar o \_ \_ sinalizador de criptografia forte do SCH \_ . no Windows 8.1, os conjuntos de codificação RC4 são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

O FIPS-Compliance tornou-se mais complexo com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS em versões anteriores desta tabela enganosa. Por exemplo, um conjunto de codificação como o TLS \_ ECDHE \_ RSA com o \_ \_ AES \_ 128 \_ CBC \_ sha256 é apenas uma reclamação de FIPS ao usar as curvas elípticas do NIST. Para descobrir quais combinações de curvas elípticas e conjuntos de codificação serão habilitados no modo FIPS, consulte a seção 3.3.1 de [diretrizes para a seleção, a configuração e o uso de implementações de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Windows 8.1 e Windows Server 2012 R2 são atualizados pelo Windows Update pela [atualização 2919355](https://support.microsoft.com/kb/2919355) aplicada, que adiciona os novos conjuntos de codificação e altera a ordem de prioridade. Os seguintes conjuntos de codificação estão habilitados e nesta ordem de prioridade por padrão pelo provedor Microsoft Schannel:



| Cadeia de caracteres do pacote de codificação                                                                                            | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P256<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P384<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                     | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/>                                                     | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                     | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/>                                                     | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                                  | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                                  | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 256 \_ GCM \_ Sha384 \_ P384<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P384<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                   | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/>                                                   | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                   | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/>                                                   | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                                                 | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                                            | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ Sha<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ SHA256 nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>            | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ \_ Sha nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>               | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5 <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5 <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/> | Yes<br/>                      | SSL 2.0<br/>                            |



 

Os seguintes conjuntos de codificação têm suporte do Microsoft Schannel Provider, mas não são habilitados por padrão:



| Cadeia de caracteres do pacote de codificação                                             | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P521<br/>   | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>      | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>      | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 256 \_ GCM \_ Sha384 \_ P521<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P521<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Yes<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>    | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>    | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ des \_ CBC \_ Sha<br/>                        | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ RC4 \_ 56 \_ Sha<br/>             | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha<br/>            | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportação RSA \_ TLS \_ com \_ RC4 \_ 40 \_ MD5<br/>                 | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ MD5 nulo<br/>                            | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ com \_ des \_ CBC \_ Sha<br/>                   | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha<br/>       | Yes<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ com \_ MD5<br/>                     | Yes<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ com \_ MD5<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

para adicionar conjuntos de codificação, use a opção política de grupo conjunto de criptografia SSL ordem em configuração do computador > Modelos Administrativos > rede > configuração ssl Configurações para configurar uma lista de prioridades para todos os conjuntos de codificação que você deseja habilitar.

 

 




