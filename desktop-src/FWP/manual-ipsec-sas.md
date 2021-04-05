---
title: SA manual
description: O cenário de diretiva IPsec SA (Associação de segurança manual) permite que os chamadores ignorem os módulos de criação de chaves IPsec (IKE e AuthIP), especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917208"
---
# <a name="manual-sa"></a>SA manual

O cenário de diretiva IPsec SA (Associação de segurança manual) permite que os chamadores ignorem os módulos de criação de chaves IPsec (IKE e AuthIP), especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.

Um exemplo de cenário SA manual possível é "adicionar um par de SA IPsec para proteger todo o tráfego de dados unicast entre os endereços IP 1.1.1.1 & 2.2.2.2, exceto ICMP, usando o modo de transporte IPsec".

> [!Note]  
> As etapas a seguir devem ser executadas em ambos os computadores com os endereços IP definidos adequadamente.

 

Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.

<dl>

**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 
    | Propriedade de filtro                                                   | Valor                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ endereço local do IP da condição FWPM \_ \_**                           | O endereço local apropriado (1.1.1.1 ou 2.2.2.2).           |
    | **\_ \_ \_ endereço IP remoto \_ da condição FWPM**                          | O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).          |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                         |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**         |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir. 
    | Propriedade de filtro                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | [**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**](filter-weight-identifiers.md)  |

        

**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**  

1.  Adicione um filtro com as propriedades a seguir. 
    | Propriedade de filtro                                                   | Valor                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                            |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ endereço IP local da condição**       | O endereço local apropriado (1.1.1.1 ou 2.2.2.2).    |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ endereço IP remoto da condição**      | O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).   |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                  |
    | **ação. calloutKey**                                             | **FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}** |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir. 
    | Propriedade de filtro                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**                                   |

        

**Configurar associações de segurança de entrada e saída**

1.  Chame [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), com o parâmetro *outboundTraffic* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de texto explicativo IPSec da camada de transporte de saída adicionado acima.
2.  Chame [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), e o parâmetro *getSpi* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de texto explicativo IPSec da camada de transporte de entrada adicionado acima. O valor SPI retornado deve ser usado como o SPI SA de entrada pelo computador local e como o SPI SA de saída pelo computador remoto correspondente. Ambos os computadores devem usar alguns meios fora de banda para trocar os valores SPI.
3.  Chame [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *INBOUNDBUNDLE* que descreve as propriedades do grupo SA de entrada (como o SPI de entrada SA, tipo de transformação, tipos de algoritmo, chaves, etc.).
4.  Chame [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *OUTBOUNDBUNDLE* que descreve as propriedades do pacote SA de saída (como o SPI de saída SA, tipo de transformação, tipos de algoritmo, chaves, etc.).

  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: chave SA manual](manual-sa-keying.md)
</dt> <dt>

[**Identificadores de texto explicativo internos**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

