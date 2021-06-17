---
description: Saiba mais sobre os conjuntos de criptografia TLS no Windows Server 2022. Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles.
title: Conjuntos de codificação TLS no Windows Server 2022.
ms.topic: article
ms.date: 02/16/2021
ms.openlocfilehash: d69cf4d97b356bf772b3a6d59a8bc4146f596ce8
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262328"
---
# <a name="tls-cipher-suites-in-windows-server-2022"></a>Conjuntos de codificação TLS no Windows Server 2022

Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles. A versão mais alta com suporte do TLS é sempre preferida no handshake de TLS.

A disponibilidade de conjuntos de codificação deve ser controlada de uma das duas maneiras:

-   A ordem de prioridade padrão é substituída quando uma lista de prioridades é configurada. Os conjuntos de codificação que não estão na lista de prioridades não serão usados.
-   Permitido quando o aplicativo passa SCH \_ usar \_ \_ criptografia forte: o provedor Microsoft Schannel filtrará pacotes de criptografia fracos conhecidos quando o aplicativo usar o \_ sinalizador de \_ criptografia forte do SCH \_ . Os conjuntos de codificação RC4, DES, exportar e nulo são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

O FIPS-Compliance tornou-se mais complexo com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS em versões anteriores desta tabela enganosa. Por exemplo, um conjunto de codificação como o TLS \_ ECDHE \_ RSA com o \_ \_ AES \_ 128 \_ CBC \_ sha256 é apenas uma reclamação de FIPS ao usar as curvas elípticas do NIST. Para descobrir quais combinações de curvas elípticas e conjuntos de codificação serão habilitados no modo FIPS, consulte a seção 3.3.1 de [diretrizes para a seleção, a configuração e o uso de implementações de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r2.pdf).

Para o Windows Server 2022, os seguintes conjuntos de codificação estão habilitados e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:



| Cadeia de caracteres do pacote de codificação                                                                           | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                               | Sim<br/>                      | TLS 1.3<br/>                            |
| TLS \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.3<br/>                            |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                               | Não<br/>                       | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                              | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                              | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                       | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                       | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                                      | Não<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ \_ SHA256 nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>       | Não<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ \_ Sha nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>          | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Os seguintes conjuntos de codificação têm suporte do Microsoft Schannel Provider, mas não são habilitados por padrão:



| Cadeia de caracteres do pacote de codificação                                                                               | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ CHACHA20 \_ POLY1305 \_ SHA256<br/>                                                        | Sim<br/>                      | TLS 1.3<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                               | Não<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
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

-   Para usar a política de grupo, configure a ordem do conjunto de codificação SSL em configuração do computador > Modelos Administrativos > rede > definições de configuração SSL com a lista de prioridades para todos os conjuntos de codificação que você deseja habilitar.
-   Para usar o PowerShell, consulte [cmdlets do TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva. O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.
