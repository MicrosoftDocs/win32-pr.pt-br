---
title: Modo de transporte
description: O cenário de política IPsec do Modo de Transporte requer proteção de modo de transporte IPsec para todo o tráfego correspondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebfb6dad27340bfc72397307c58fddfe2bdf6eeadb65081faa0e1941de2c052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535886"
---
# <a name="transport-mode"></a>Modo de transporte

O cenário de política IPsec do Modo de Transporte requer proteção de modo de transporte IPsec para todo o tráfego correspondente. Qualquer tráfego de texto não limpo correspondente é descartado até que a negociação IKE ou AuthIP seja concluída com êxito. Se a negociação falhar, a conectividade com o endereço IP correspondente permanecerá interrompida.

Um exemplo de um possível cenário de Modo de Transporte é "Proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec".

Para implementar este exemplo programaticamente, use a seguinte configuração do WFP.

<dl>

**Em FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} configurar política de negociação mm**  

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

        

**Em FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} configurar política de negociação de QM e EM**  

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM.  
    -   Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSEC \_ IKE \_ QM \_ TRANSPORT \_ CONTEXT**.
    -   Para o AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT**. Opcionalmente, esse contexto pode conter a política de negociação em modo estendido AuthIP.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política de QM correspondente será aplicada. AuthIP é o módulo de chave preferencial se há suporte para IKE e AuthIP.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor de QM adicionado na etapa 1. |

        

**Em FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} configure regras de filtragem de entrada por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 

    | Propriedade Filter                                                   | Valor                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **action.type**                                                   | TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_                             |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}             |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                  | Valor                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                               |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**            | IPPROTO \_ ICMP{V6}Essas constantes são definidas em winsock2.h.<br/>    |
    | **action.type**                                                  | PERMISSÃO DE AÇÃO \_ FWP \_                                                       |
    | **weight**                                                       | [**ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md) |

        

**Em FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} configure regras de filtragem de saída por pacote**  

1.  Adicione um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                        |
    | **action.type**                                                   | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**              |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                            |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | IPPROTO \_ ICMP{V6}Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | PERMISSÃO DE AÇÃO \_ FWP \_                                                    |
    | **weight**                                                        | ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_                                   |

        

</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: usando o modo de transporte](using-transport-mode.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Tipos de contexto do provedor**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Condições de filtragem](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificadores de callout integrados**](built-in-callout-identifiers.md)
</dt> </dl>

 

