---
description: Saiba mais sobre os suites de criptografia TLS Windows 10 v1709. Os suites de criptografia só podem ser negociados para versões TLS que os suportam.
ms.assetid: E1E731F9-1F17-4252-ADDB-22742344C37B
title: Conjunto de Criptografia TLS Windows 10 v1709
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105a11d601cd672ff2620c43609b7b57ce4d356889f670e15726b8f18569fde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786175"
---
# <a name="tls-cipher-suites-in-windows-10-v1709"></a>Conjunto de Criptografia TLS Windows 10 v1709

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Os suites de criptografia só podem ser negociados para versões TLS que os suportam. A versão TLS com suporte mais alta é sempre preferencial no handshake do TLS.

A disponibilidade de conjunto de criptografias deve ser controlada de duas maneiras:

-   A ordem de prioridade padrão é substituído quando uma lista de prioridade é configurada. Os suites de criptografia que não estão na lista de prioridade não serão usados.
-   Permitido quando o aplicativo passar SCH USE STRONG CRYPTO: o provedor \_ \_ do Microsoft Schannel filtrará os suites de criptografia fracos conhecidos quando o aplicativo usar o sinalizador \_ SCH \_ USE STRONG \_ \_ CRYPTO. Rc4, DES, exportar e conjunto de criptografias nulos são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com os suites de criptografia não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com navegadores e clientes HTTP/2, consulte [Como implantar a ordenação personalizada do conjunto de criptografias.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

A conformidade com FIPS tornou-se mais complexa com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS nas versões anteriores desta tabela enganosa. Por exemplo, um conjunto de criptografias como TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC SHA256 é apenas uma reclamações \_ FIPS ao usar curvas elípticas NIST. Para descobrir quais combinações de curvas elípticas e de conjunto de codificação serão habilitadas no modo FIPS, consulte a seção 3.3.1 de Diretrizes para seleção, configuração e uso de implementações [TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Por Windows 10, versão 1709, os seguintes pacote de criptografia estão habilitados e, por padrão, nessa ordem de prioridade usando o Provedor Schannel da Microsoft:



| Cadeia de caracteres do conjunto de criptografias                                                                                 | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versões do protocolo TLS/SSL                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                              | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                              | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                       | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                       | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                      | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ NULL \_ SHA256 <br/> Usado somente quando o aplicativo solicita explicitamente.<br/> | Não<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA COM SHA \_ \_ \_ NULO <br/> Usado somente quando o aplicativo solicita explicitamente.<br/>    | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Os seguintes pacote de codificação têm suporte do Provedor Schannel da Microsoft, mas não são habilitados por padrão:



| Cadeia de caracteres do conjunto de criptografias                                                                               | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versões do protocolo TLS/SSL                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                               | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ Sha<br/>                                                          | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ MD5<br/>                                                          | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ des \_ CBC \_ Sha<br/>                                                          | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ com \_ des \_ CBC \_ Sha<br/>                                                     | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ com \_ DES \_ CBC \_ Sha não TLS 1,2, tls 1,1, TLS 1,0, SSL 3,0<br/>   | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ MD5 nulo <br/> Usado apenas quando o aplicativo solicita explicitamente. <br/> | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ RC4 \_ 56 \_ Sha<br/>                                               | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportação RSA \_ TLS \_ com \_ RC4 \_ 40 \_ MD5<br/>                                                   | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha<br/>                                              | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Os seguintes conjuntos de codificação PSK estão habilitados e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:



| Cadeia de caracteres do pacote de codificação                              | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ com \_ AES \_ 256 \_ CBC \_ Sha384<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| Protocolo \_ TLS \_ PSK \_ com \_ Sha384 nulo<br/>          | Não<br/>                       | TLS 1.2<br/>        |
| Protocolo TLS \_ PSK \_ com \_ nulo \_ SHA256<br/>          | Não<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Não há conjuntos de codificação PSK habilitados por padrão. Os aplicativos precisam solicitar PSK usando SCH \_ usam \_ \_ apenas PRESHAREDKEY. Para obter mais informações sobre sinalizadores Schannel, consulte [**Schannel \_ creds**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Para adicionar conjuntos de codificação, implante uma política de grupo ou use os cmdlets TLS:

-   para usar a política de grupo, configure a ordem do conjunto de codificação ssl em configuração do computador > Modelos Administrativos > rede > configuração ssl Configurações com a lista de prioridade para todos os conjuntos de codificação que você deseja habilitar.
-   Para usar o PowerShell, consulte [cmdlets do TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> antes da Windows 10, as cadeias de caracteres do conjunto de codificação foram anexadas à curva elíptica para determinar a prioridade da curva. o Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a política de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.

 

 

 
