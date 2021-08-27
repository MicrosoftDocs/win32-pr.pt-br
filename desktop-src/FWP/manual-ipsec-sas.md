---
title: Manual SA
description: O cenário de política de IPsec da SA (Associação de Segurança Manual) permite que os chamadores ignorem os módulos de chave IPsec (IKE e AuthIP) integrados especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cdb3d7c67d9cfa513cbdff846c02fd6ba61ebf031672fb86887bc01c90455b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083316"
---
# <a name="manual-sa"></a>Manual SA

O cenário de política de IPsec da SA (Associação de Segurança Manual) permite que os chamadores ignorem os módulos de chave IPsec (IKE e AuthIP) integrados especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.

Um exemplo de um possível cenário sa manual é "Adicionar um par SA IPsec para proteger todo o tráfego de dados unicast entre os endereços IP 1.1.1.1 & 2.2.2.2, exceto ICMP, usando o modo de transporte IPsec".

> [!Note]  
> As etapas a seguir devem ser executadas em ambos os máquinas com endereços IP definidos adequadamente.

 

Para implementar este exemplo programaticamente, use a seguinte configuração do WFP.

<dl>

**Em FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} configure regras de filtragem de entrada por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **ENDEREÇO IP LOCAL DA CONDIÇÃO DO FWPM \_ \_ \_ \_**                           | O endereço local apropriado (1.1.1.1 ou 2.2.2.2).           |
    | **ENDEREÇO REMOTO IP DA CONDIÇÃO DO FWPM \_ \_ \_ \_**                          | O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).          |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                         |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**         |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISSÃO DE AÇÃO \_ FWP \_**                                                    |
    | **weight**                                                        | [**ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**Em FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} configure regras de filtragem de saída por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                            |
    | **FWPM \_ Condição de \_ \_ filtragem \_ DE ENDEREÇO LOCAL DO IP** CONDITION       | O endereço local apropriado (1.1.1.1 ou 2.2.2.2).    |
    | **FWPM \_ Condição de \_ \_ filtragem \_ de ENDEREÇO REMOTO IP** CONDITION      | O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).   |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                  |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6}** |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISSÃO DE AÇÃO \_ FWP \_**                                                    |
    | **weight**                                                        | **ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**                                   |

        

**Configurar associações de segurança de entrada e saída**

1.  Chame [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), com o parâmetro *outboundTraffic* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de texto explicador IPsec da camada de transporte de saída adicionado acima.
2.  Chame [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), com o parâmetro *id* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *getSpi* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de chamada IPsec da camada de transporte de entrada adicionado acima. O valor spi retornado deve ser usado como a SPI SA de entrada pelo computador local e como a SPI SA de saída pelo computador remoto correspondente. Ambas as máquinas devem usar alguns meios fora de banda para trocar os valores da SPI.
3.  Chame [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), com o parâmetro *id* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *inboundBundle* que descreve as propriedades do pacote SA de entrada (como a SPI SA de entrada, tipo de transformação, tipos de algoritmo, chaves etc).
4.  Chame [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0),  com o parâmetro id que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *outboundBundle* que descreve as propriedades do pacote SA de saída (como a SPI SA de saída, tipo de transformação, tipos de algoritmo, chaves etc).

  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: Chave SA manual](manual-sa-keying.md)
</dt> <dt>

[**Identificadores de callout integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

