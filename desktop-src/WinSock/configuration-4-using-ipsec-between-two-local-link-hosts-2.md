---
description: Essa configuração cria uma associação de segurança (SA) IPsec entre dois hosts na mesma sub-rede para realizar a autenticação usando o algoritmo de hash Cabeçalho de Autenticação (AH) e Message Digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configuração 3: usando o IPsec entre dois hosts de link local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b72485db34e8ff2c4e29a201df258dfb9d2ab9a00717ab515cda982e7ea867dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121426"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configuração 3: usando o IPsec entre dois hosts de link local

Essa configuração cria uma associação de segurança (SA) IPsec entre dois hosts na mesma sub-rede para realizar a autenticação usando o algoritmo de hash Cabeçalho de Autenticação (AH) e Message Digest 5 (MD5). Neste exemplo, a configuração mostrada protege todo o tráfego entre dois hosts vizinhos: host 1, com o endereço de link local FE80:: 2AA: FF: FE53: A92C e host 2, com o endereço de link local FE80:: 2AA: FF: FE92: D0F1.

**Para usar o IPsec entre dois hosts de link local**

1.  No host 1, Crie arquivos de associação de segurança em branco (SAD) e de política de segurança (SPD) usando o comando ipsec6 c. Neste exemplo, o comando Ipsec6.exe é Ipsec6 c Test. Isso cria dois arquivos para configurar manualmente associações de segurança (Test. Sad) e políticas de segurança (Test. SPD).
2.  No host 1, edite o arquivo SPD para adicionar uma política de segurança que protege todo o tráfego entre o host 1 e o host 2.

    A tabela a seguir mostra a política de segurança adicionada ao arquivo Test. SPD antes da primeira entrada para este exemplo (a primeira entrada no arquivo Test. SPD não foi modificada).

    | Nome do campo de arquivo SPD | Valor de exemplo              |
    |---------------------|----------------------------|
    | **Política**          | 2                          |
    | **RemoteIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **NELES**                     |
    | **IPSecmode**       | **PORTA**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direção**       | **Bidirect**               |
    | **Ação**          | **USAR**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Coloque um ponto e vírgula no final da linha Configurando essa política de segurança. As entradas de política devem ser colocadas em ordem numérica decrescente.

3.  No host 1, edite o arquivo triste, adicionando entradas SA para proteger todo o tráfego entre o host 1 e o host 2. Duas associações de segurança devem ser criadas, uma para o tráfego para o host 2 e outra para o tráfego do host 2.

    A tabela a seguir mostra a primeira entrada SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego para o host 2).

    | Nome do campo de arquivo triste | Valor de exemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **DestIPAddr**      | **POLÍTICA**                 |
    | **SrcIPAddr**       | **POLÍTICA**                 |
    | **Protocolo**        | **POLÍTICA**                 |
    | **DestPort**        | **POLÍTICA**                 |
    | **SrcPort**         | **POLÍTICA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Direção**       | **SA**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque um ponto e vírgula no final da linha Configurando esse SA.

    A tabela a seguir mostra a segunda entrada SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego do host 2).

    | Nome do campo de arquivo triste | Valor de exemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **DestIPAddr**      | **POLÍTICA**                 |
    | **SrcIPAddr**       | **POLÍTICA**                 |
    | **Protocolo**        | **POLÍTICA**                 |
    | **DestPort**        | **POLÍTICA**                 |
    | **SrcPort**         | **POLÍTICA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Direção**       | **ENTRADA**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque um ponto e vírgula no final da linha Configurando esse SA. As entradas SA devem ser colocadas em ordem numérica decrescente.

4.  No host 1, crie um arquivo de texto que contenha uma cadeia de texto usada para autenticar a SAs criada com o host 2. Neste exemplo, o arquivo Test. Key é criado com o conteúdo "Este é um teste". Você deve incluir aspas duplas em volta da cadeia de caracteres de chave para que a chave seja lida pela ferramenta Ipsec6.

    O Microsoft IPv6 Technology Preview só dá suporte a chaves configuradas manualmente para a autenticação de SAs IPsec. As chaves manuais são configuradas criando arquivos de texto que contêm a cadeia de caracteres de texto da chave manual. Neste exemplo, a mesma chave para as SAs é usada em ambas as direções. Você pode usar chaves diferentes para SAs de entrada e saída criando arquivos de chave diferentes e referenciando-os com o campo KeyFile no arquivo SAD.

5.  No Host 2, crie arquivos SAD (associação de segurança em branco) e spd (política de segurança) usando o comando ipsec6 c. Neste exemplo, o comando Ipsec6.exe é ipsec6 c test. Isso cria dois arquivos com entradas em branco para configurar manualmente associações de segurança (Test.sad) e políticas de segurança (Test.spd).

    Para simplificar o exemplo, os mesmos nomes de arquivo para os arquivos SAD e SPD são usados no Host 2. Você pode optar por usar nomes de arquivo diferentes em cada host.

6.  No Host 2, edite o arquivo SPD para adicionar uma política de segurança que proteja todo o tráfego entre o Host 2 e o Host 1.

    A tabela a seguir mostra a entrada de política de segurança adicionada antes da primeira entrada ao arquivo Test.spd para este exemplo (a primeira entrada no arquivo Test.spd não foi modificada).

    | Nome do campo de arquivo SPD | Valor de exemplo              |
    |---------------------|----------------------------|
    | **Política**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AH**                     |
    | **IPSecMode**       | **Transporte**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direção**       | **BIDIRECT**               |
    | **Ação**          | **Aplicar**                  |
    | **Interfaceindex**  | 0                          |

    

     

    Coloque um ponto e vírgula no final da linha configurando essa política de segurança. As entradas de política devem ser colocadas em ordem numérica decrescente.

7.  No Host 2, edite o arquivo SAD, adicionando entradas SA para proteger todo o tráfego entre o Host 2 e o Host 1. Duas associações de segurança devem ser criadas– uma para o tráfego para o Host 1 e outra para o tráfego do Host 1.

    A tabela a seguir mostra o primeiro SA adicionado ao arquivo Test.sad para este exemplo (para tráfego do Host 1).

    | Nome do campo de arquivo SAD | Valor de exemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **POLÍTICA**                 |
    | **SrcIPAddr**       | **POLÍTICA**                 |
    | **Protocolo**        | **POLÍTICA**                 |
    | **DestPort**        | **POLÍTICA**                 |
    | **SrcPort**         | **POLÍTICA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Direção**       | **Entrada**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque um ponto e vírgula no final da linha configurando esse SA.

    A tabela a seguir mostra a segunda entrada SA adicionada ao arquivo Test.sad para este exemplo (para tráfego para o Host 1).

    | Nome do campo de arquivo SAD | Valor de exemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **POLÍTICA**                 |
    | **SrcIPAddr**       | **POLÍTICA**                 |
    | **Protocolo**        | **POLÍTICA**                 |
    | **DestPort**        | **POLÍTICA**                 |
    | **SrcPort**         | **POLÍTICA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Direção**       | **Saída**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque um ponto e vírgula no final da linha configurando esse SA. As entradas SA devem ser colocadas em ordem numérica decrescente.

8.  No Host 2, crie um arquivo de texto que contém uma cadeia de caracteres de texto usada para autenticar as SAs criadas com o Host 1. Neste exemplo, o arquivo Test.key é criado com o conteúdo "Este é um teste". Você deve incluir aspas duplas em torno da cadeia de caracteres de chave para que a chave seja lida pela ferramenta ipsec6.
9.  No Host 1, adicione as políticas de segurança configuradas e as SAs dos arquivos SPD e SAD usando o comando ipsec6 a. Neste exemplo, o ipsec6 um comando de teste é executado no Host 1.
10. No Host 2, adicione as políticas de segurança configuradas e as SAs dos arquivos SPD e SAD usando o comando ipsec6 a. Neste exemplo, o ipsec6 um comando de teste é executado no Host 2.
11. Ping host 1 do Host 2 com o comando ping6.

    Se você capturar o tráfego usando Monitor de Rede da Microsoft ou outro farejador de pacotes, deverá ver a troca de mensagens de Solicitação de Eco ICMPv6 e Resposta de Eco com um Cabeçalho de Autenticação entre o header IPv6 e o header ICMPv6.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Sub-rede única com endereços locais de link](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Tráfego IPv6 entre nós em diferentes sub-redes de uma internet IPv4 (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



