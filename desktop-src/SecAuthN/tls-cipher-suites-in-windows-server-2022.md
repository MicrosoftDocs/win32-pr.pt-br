---
description: saiba mais sobre conjuntos de codificação TLS no Windows Server 2022. Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles.
title: conjuntos de codificação TLS no Windows Server 2022.
ms.topic: article
ms.date: 02/16/2021
ms.openlocfilehash: 10f49c18838b8e727f590505dd7af86203f882106ce351c559b6d687f8dd824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785966"
---
# <a name="tls-cipher-suites-in-windows-server-2022"></a>conjuntos de codificação TLS no Windows Server 2022

Os conjuntos de codificação só podem ser negociados para versões de TLS que dão suporte a eles. A versão mais alta com suporte do TLS é sempre preferida no handshake de TLS.

A disponibilidade de conjuntos de codificação deve ser controlada de uma das duas maneiras:

-   A ordem de prioridade padrão é substituída quando uma lista de prioridades é configurada. Os conjuntos de codificação que não estão na lista de prioridades não serão usados.
-   Permitido quando o aplicativo passa SCH \_ usar \_ \_ criptografia forte: o provedor Microsoft Schannel filtrará pacotes de criptografia fracos conhecidos quando o aplicativo usar o \_ sinalizador de \_ criptografia forte do SCH \_ . Os conjuntos de codificação RC4, DES, exportar e nulo são filtrados.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

O FIPS-Compliance tornou-se mais complexo com a adição de curvas elípticas, tornando a coluna habilitada para o modo FIPS em versões anteriores desta tabela enganosa. Por exemplo, um conjunto de codificação como o TLS \_ ECDHE \_ RSA com o \_ \_ AES \_ 128 \_ CBC \_ sha256 é apenas uma reclamação de FIPS ao usar as curvas elípticas do NIST. Para descobrir quais combinações de curvas elípticas e conjuntos de codificação serão habilitados no modo FIPS, consulte a seção 3.3.1 de [diretrizes para a seleção, a configuração e o uso de implementações de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r2.pdf).

para o Windows Server 2022, os seguintes conjuntos de codificação estão habilitados e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:



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
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sim<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sim<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                               | Não<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ SHA<br/>                                                          | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ MD5<br/>                                                          | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ DES \_ CBC \_ SHA<br/>                                                          | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ WITH \_ DES \_ CBC \_ SHA<br/>                                                     | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ WITH \_ DES \_ CBC SHA No \_ TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/>   | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ COM \_ \_ MD5 NULO <br/> Usado somente quando o aplicativo solicita explicitamente. <br/> | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ WITH \_ RC4 \_ 56 \_ SHA<br/>                                               | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| EXPORTAÇÃO DE RSA TLS \_ \_ COM \_ \_ RC4 \_ 40 \_ MD5<br/>                                                   | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ WITH \_ DES \_ CBC \_ SHA<br/>                                              | Não<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Os seguintes pacote de criptografia PSK estão habilitados e, por padrão, nessa ordem de prioridade usando o Provedor Schannel da Microsoft:



| Cadeia de caracteres do conjunto de criptografias                              | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versões do protocolo TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Sim<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ COM \_ \_ SHA384 NULO<br/>          | Não<br/>                       | TLS 1.2<br/>        |
| TLS \_ PSK \_ WITH \_ NULL \_ SHA256<br/>          | Não<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Nenhum pacote de criptografia PSK está habilitado por padrão. Os aplicativos precisam solicitar PSK usando SCH \_ USE \_ PRESHAREDKEY \_ SOMENTE. Para obter mais informações sobre sinalizadores Schannel, consulte [**SCHANNEL \_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Para adicionar conjunto de criptografias, implante uma política de grupo ou use os cmdlets TLS:

-   Para usar a política de grupo, configure o Pedido do Pacote de Criptografia SSL em Configuração do Computador > Modelos Administrativos > Network > Configuração de SSL Configurações com a lista de prioridade para todos os pacote de criptografia que você deseja habilitar.
-   Para usar o PowerShell, consulte [Cmdlets TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Antes de Windows 10, as cadeias de caracteres do conjunto de criptografias eram anexadas com a curva elíptica para determinar a prioridade da curva. Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica para que o sufixo de curva elíptica não seja necessário e seja substituído pela nova ordem de prioridade de curva elíptica, quando fornecido, para permitir que as organizações usem a política de grupo para configurar versões diferentes do Windows com os mesmos grupos de criptografia.
