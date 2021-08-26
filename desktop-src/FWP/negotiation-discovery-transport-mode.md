---
title: Modo de transporte de descoberta de negociação
description: O cenário de política IPsec do Modo de Transporte de Descoberta de Negociação requer proteção de modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita proteção IPsec para correspondência de tráfego de saída.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990a7f84e20d081933ffa0def9800ff7610a3a0e3a6d01dd3b45fe7c99729ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102136"
---
# <a name="negotiation-discovery-transport-mode"></a>Modo de transporte de descoberta de negociação

O cenário de política IPsec do Modo de Transporte de Descoberta de Negociação requer proteção de modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita proteção IPsec para correspondência de tráfego de saída. Portanto, as conexões de saída têm permissão para fazer fallback para texto não limpo enquanto as conexões de entrada não são.

Com essa política, quando o computador host tenta uma nova conexão de saída e não há NENHUMA SA IPsec existente correspondente ao tráfego, o host envia simultaneamente os pacotes em texto não escrito e inicia uma negociação IKE ou AuthIP. Se a negociação for bem-sucedida, a conexão será atualizada para protegida por IPsec. Caso contrário, a conexão permanecerá em texto não escrito. Depois de protegida por IPsec, uma conexão nunca poderá ser downgrade para texto não limpo.

O Modo de Transporte de Descoberta de Negociação normalmente é usado em ambientes que incluem máquinas com capacidade IPsec e não IPsec.

Um exemplo de um possível cenário de Modo de Transporte de Descoberta de Negociação é "Proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec e habilitar a descoberta de negociação".

Para implementar este exemplo programaticamente, use a seguinte configuração do WFP.

<dl>

**Em FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} configurar a política de negociação mm**  

1.  Adicione um ou ambos os seguintes contextos do provedor de política MM.  
    -   Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**.
    -   Para o AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política mm correspondente será aplicada. AuthIP é o módulo de chave preferencial se há suporte para IKE e AuthIP.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor MM adicionado na etapa 1. |

        

**Em FWPM \_ LAYER \_ IPSEC \_ V{4 6} configurar política de negociação \| de QM e EM**  

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e de definido o sinalizador [**\_ \_ \_ ND \_ SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) do SINALIZADOR DE POLÍTICA IPSEC.  
    -   Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSEC \_ IKE \_ QM \_ TRANSPORT \_ CONTEXT.
    -   Para o AuthIP, um contexto de provedor de política do tipo FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT. Opcionalmente, esse contexto pode conter a política de negociação em modo estendido AuthIP.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política de QM correspondente será aplicada. AuthIP é o módulo de chave preferencial se há suporte para IKE e AuthIP.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor de QM adicionado na etapa 1. |

        

**Em FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} configurar regras de filtragem de entrada por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                                                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**                                              |
    | **rawContext**                                                    | [**SEGURANÇA DE CONEXÃO DE PERSISTÊNCIA DE \_ \_ IPSEC \_ DE \_ \_ \_ CONTEXTO DO FWPM**](filter-context-identifiers.md) |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISSÃO DE AÇÃO \_ FWP \_**                                                    |
    | **weight**                                                        | [**ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**Em FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} configurar regras de filtragem de saída por pacote**  

1.  Adicione um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ IPSEC \_ OUTBOUND \_ NEGOTIATE \_ DISCOVER**](filter-context-identifiers.md) |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISSÃO DE AÇÃO \_ FWP \_**                                                    |
    | **weight**                                                        | **ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**                                   |

        

**Em FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} configurar regras de filtragem de entrada por conexão**  

1.  Adicione um filtro com as propriedades a seguir. Esse filtro só permitirá tentativas de conexão de entrada se elas são protegidas pelo IPsec. 

    | Propriedade Filter                                                   | Valor                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                  |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V{4 \| 6}** |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**                                   |

        

</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: usando o modo de transporte](using-transport-mode.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[**Identificadores de texto explicativo internos**](built-in-callout-identifiers.md)
</dt> <dt>

[Condições de filtragem](filtering-conditions.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_tipo de \_ contexto do provedor FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

