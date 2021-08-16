---
description: Saiba mais sobre os suites de criptografia TLS Windows 7. Os suites de criptografia só podem ser negociados para versões TLS que os suportam.
ms.assetid: 283CB634-25EA-47F5-A2E3-0913F7D3D9DC
title: Conjunto de Criptografia TLS no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec429fa3175c93da20dedd4e0b55905b6d3bd0cbe5aceb0872b7ec065ecc6064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785996"
---
# <a name="tls-cipher-suites-in-windows-7"></a>Conjunto de Criptografia TLS no Windows 7

Os suites de criptografia só podem ser negociados para versões TLS que os suportam. A versão TLS com suporte mais alta é sempre preferencial no handshake do TLS. Por exemplo, o SSL CK RC4 128 WITH MD5 só pode ser usado quando o cliente e o servidor não têm suporte para \_ \_ \_ \_ \_ TLS 1.2, 1.1 & 1.0 ou SSL 3.0, pois ele só tem suporte com SSL 2.0.

A disponibilidade de conjunto de criptografias deve ser controlada de duas maneiras:

-   A ordem de prioridade padrão é substituído quando uma lista de prioridade é configurada. Os suites de criptografia que não estão na lista de prioridade não serão usados.
-   Permitido quando o aplicativo passa SCH USE STRONG CRYPTO: o provedor \_ \_ do Microsoft Schannel filtrará os suites de criptografia fracos conhecidos quando o aplicativo usar o sinalizador \_ SCH \_ USE STRONG \_ \_ CRYPTO. No Windows 7, os pacote de criptografia RC4 são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com os suites de criptografia não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com navegadores e clientes HTTP/2, consulte [Como implantar a ordenação personalizada do conjunto de criptografias.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

A conformidade com FIPS tornou-se mais complexa com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS nas versões anteriores desta tabela enganosa. Por exemplo, um conjunto de criptografias, como TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 CBC SHA256, só é compatível com FIPS ao usar curvas \_ \_ elípticas NIST. Para descobrir quais combinações de curvas elípticas e de conjunto de codificação serão habilitadas no modo FIPS, consulte a seção 3.3.1 de Diretrizes para seleção, configuração e uso de implementações [TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Windows 7, Windows 8 e Windows Server 2012 são atualizados pelo Windows Update pelo 3042058 que altera a ordem de prioridade. Consulte [Microsoft Security Advisory 3042058](/security-updates/SecurityAdvisories/2015/3042058) para obter mais informações. Os seguintes pacote de criptografia estão habilitados e, por padrão, nessa ordem de prioridade pelo Provedor Schannel da Microsoft:



| Cadeia de caracteres do conjunto de criptografias                                                                                            | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versões do protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                     | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                     | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                     | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                     | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ SHA<br/>                                                                       | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ NULL \_ SHA256 <br/> Usado somente quando o aplicativo solicita explicitamente.<br/>            | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA COM SHA \_ \_ \_ NULO <br/> Usado somente quando o aplicativo solicita explicitamente.<br/>               | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5 <br/> Usado somente quando o aplicativo solicita explicitamente.<br/>            | Não<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ COM \_ MD5 <br/> Usado somente quando o aplicativo solicita explicitamente.<br/> | Sim<br/>                      | SSL 2.0<br/>                            |



 

Os seguintes pacote de codificação têm suporte do Provedor Schannel da Microsoft, mas não são habilitados por padrão:



| Cadeia de caracteres do conjunto de criptografias                                             | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versões do protocolo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>      | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>      | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>    | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>    | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ DES \_ CBC \_ SHA<br/>                        | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ WITH \_ RC4 \_ 56 \_ SHA<br/>             | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ WITH \_ DES \_ CBC \_ SHA<br/>            | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| EXPORTAÇÃO DE RSA TLS \_ \_ COM \_ \_ RC4 \_ 40 \_ MD5<br/>                 | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ COM \_ \_ MD5 NULO<br/>                            | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ WITH \_ DES \_ CBC \_ SHA<br/>                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ WITH \_ DES \_ CBC \_ SHA<br/>       | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC \_ COM \_ MD5<br/>                     | Sim<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5<br/>               | Não<br/>                       | SSL 2.0<br/>                            |



 

Para adicionar conjunto de criptografias, use a configuração de política de grupo Ordem do Conjunto de Criptografia SS > Modelos Administrativos > L em Configuração do Computador > Network > Configuração de SSL Configurações para configurar uma lista de prioridade para todos os pacote de criptografia que você deseja habilitar.

 

 
