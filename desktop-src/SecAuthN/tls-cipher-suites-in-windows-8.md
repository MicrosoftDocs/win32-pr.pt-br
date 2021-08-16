---
description: Saiba mais sobre os conjuntos de codificação TLS no Windows 8. Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles.
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: Conjuntos de codificação TLS no Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2761098142d82f37c3bb22dd038bb2dc158155c12db8ca5ad31887f2f4724a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785986"
---
# <a name="tls-cipher-suites-in-windows-8"></a>Conjuntos de codificação TLS no Windows 8

Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles. A versão mais alta com suporte do TLS é sempre preferida no handshake de TLS. Por exemplo, SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5 só pode ser usado quando o cliente e o servidor não dão suporte a TLS 1,2, 1,1 & 1,0 ou SSL 3,0, pois ele só tem suporte com SSL 2,0.

A disponibilidade de conjuntos de codificação deve ser controlada de uma das duas maneiras:

-   A ordem de prioridade padrão é substituída quando uma lista de prioridades é configurada. Os conjuntos de codificação que não estão na lista de prioridades não serão usados.
-   Permitido quando o aplicativo passa \_ SCH \_ usar \_ criptografia forte: o provedor Microsoft Schannel filtrará pacotes de criptografia fracos conhecidos quando o aplicativo usar o \_ \_ sinalizador de criptografia forte do SCH \_ . no Windows 8, os conjuntos de codificação RC4 são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

O FIPS-Compliance tornou-se mais complexo com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS em versões anteriores desta tabela enganosa. Por exemplo, um conjunto de codificação como o TLS \_ ECDHE \_ RSA com o \_ \_ AES \_ 128 \_ CBC \_ sha256 é apenas uma reclamação de FIPS ao usar as curvas elípticas do NIST. Para descobrir quais combinações de curvas elípticas e conjuntos de codificação serão habilitados no modo FIPS, consulte a seção 3.3.1 de [diretrizes para a seleção, a configuração e o uso de implementações de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Windows 7, Windows 8 e Windows Server 2012 são atualizados pelo Windows Update pela atualização 3042058, que altera a ordem de prioridade. Consulte [o comunicado de segurança da Microsoft 3042058](/security-updates/SecurityAdvisories/2015/3042058) para obter mais informações. Os seguintes conjuntos de codificação estão habilitados e nesta ordem de prioridade por padrão pelo provedor Microsoft Schannel:



| Cadeia de caracteres do pacote de codificação                                                                                            | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P256<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P384<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                     | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/>                                                     | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                     | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/>                                                     | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                                  | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                                  | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 256 \_ GCM \_ Sha384 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                   | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/>                                                   | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                   | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/>                                                   | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
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

 

 
