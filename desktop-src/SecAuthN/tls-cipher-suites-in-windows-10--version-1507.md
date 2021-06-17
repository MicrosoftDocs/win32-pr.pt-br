---
description: Saiba mais sobre os conjuntos de criptografia TLS no Windows 10 v1507. Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles.
ms.assetid: 58A47273-D2D3-449D-891C-C9502012C557
title: Conjuntos de codificação TLS no Windows 10 v1507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c974f03c1f7dbe8314820224b70f14ea7121b9
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262538"
---
# <a name="tls-cipher-suites-in-windows-10-v1507"></a>Conjuntos de codificação TLS no Windows 10 v1507

Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles. A versão mais alta com suporte do TLS é sempre preferida no handshake de TLS. Por exemplo, SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5 só pode ser usado quando o cliente e o servidor não dão suporte a TLS 1,2, 1,1 & 1,0 ou SSL 3,0, pois ele só tem suporte com SSL 2,0.

A disponibilidade de conjuntos de codificação deve ser controlada de uma das duas maneiras:

-   A ordem de prioridade padrão é substituída quando uma lista de prioridades é configurada. Os conjuntos de codificação que não estão na lista de prioridades não serão usados.
-   Permitido quando o aplicativo passa \_ SCH \_ usar \_ criptografia forte: o provedor Microsoft Schannel filtrará pacotes de criptografia fracos conhecidos quando o aplicativo usar o \_ \_ sinalizador de criptografia forte do SCH \_ . No Windows 10, versão 1507, os conjuntos de codificação RC4 são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

O FIPS-Compliance tornou-se mais complexo com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS em versões anteriores desta tabela enganosa. Por exemplo, um conjunto de codificação como o TLS \_ ECDHE \_ RSA com o \_ \_ AES \_ 128 \_ CBC \_ sha256 é apenas uma reclamação de FIPS ao usar as curvas elípticas do NIST. Para descobrir quais combinações de curvas elípticas e conjuntos de codificação serão habilitados no modo FIPS, consulte a seção 3.3.1 de [diretrizes para a seleção, a configuração e o uso de implementações de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Para o Windows 10, versão 1507, os seguintes conjuntos de codificação estão habilitados e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:



| Cadeia de caracteres do pacote de codificação                                                                                            | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                        | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                        | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384<br/>                                                        | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                        | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                           | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                           | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                                  | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                                  | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 256 \_ GCM \_ Sha384<br/>                                                      | Sim<br/>                      | TLS 1.2<br/>                            |
| \_ECDHE \_ de TLS \_ de ECDSA com \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                      | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha384<br/>                                                      | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                      | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                         | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                         | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                                                 | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>                                                            | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ Sha<br/>                                                                       | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ SHA256 nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>            | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ com \_ \_ Sha nulo <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>               | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5 <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/>            | Não<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5 <br/> Usado apenas quando o aplicativo solicita explicitamente.<br/> | Sim<br/>                      | SSL 2.0<br/>                            |



 

Os seguintes conjuntos de codificação têm suporte do Microsoft Schannel Provider, mas não são habilitados por padrão:



| Cadeia de caracteres do pacote de codificação                                                                  | Permitido pelo SCH \_ usar \_ \_ criptografia forte | Versões do protocolo TLS/SSL                     |
|--------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ RSA \_ com \_ des \_ CBC \_ Sha<br/>                                             | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ RC4 \_ 56 \_ Sha<br/>                                  | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha<br/>                                 | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportação RSA \_ TLS \_ com \_ RC4 \_ 40 \_ MD5<br/>                                      | Não<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ MD5 nulo usado somente quando o aplicativo solicita explicitamente.<br/> | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ com \_ des \_ CBC \_ Sha<br/>                                        | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha<br/>                            | Sim<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ com \_ MD5<br/>                                          | Sim<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ com \_ MD5<br/>                                    | Não<br/>                       | SSL 2.0<br/>                            |



 

Para adicionar conjuntos de codificação, implante uma política de grupo ou use os cmdlets TLS:

-   Para usar a política de grupo, configure a ordem do conjunto de codificação SSL em configuração do computador > Modelos Administrativos > rede > definições de configuração SSL com a lista de prioridades para todos os conjuntos de codificação que você deseja habilitar.
-   Para usar o PowerShell, consulte [cmdlets do TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva. O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.

 

> [!IMPORTANT]
> Os serviços Web HTTP/2 são incompatíveis com pedidos personalizados de conjunto de criptografia TLS. Para obter mais informações, consulte [como implantar a ordenação do conjunto de codificação personalizado](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

 

 
