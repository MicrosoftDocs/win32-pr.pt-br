---
title: Criptografia Garantida
description: O cenário de política de IPsec de Criptografia Garantida requer criptografia IPsec para todo o tráfego correspondente. Essa política deve ser especificada em conjunto com uma das opções de política de modo de transporte.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d029b3bebc6fc6e0a438c5123bb6703bc45dd457195fa7ff8fc7268bba16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069146"
---
# <a name="guaranteed-encryption"></a>Criptografia Garantida

O cenário de política de IPsec de Criptografia Garantida requer criptografia IPsec para todo o tráfego correspondente. Essa política deve ser especificada em conjunto com uma das opções de política de modo de transporte.

A Criptografia Garantida normalmente é usada para criptografar tráfegos confidenciais por aplicativo.

Um exemplo de um possível cenário de Criptografia Garantida é "Proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec, habilitar a descoberta de negociação e exigir criptografia garantida para todo o tráfego unicast correspondente à porta local TCP 5555".

Para implementar este exemplo programaticamente, use a seguinte configuração do WFP.

<dl>

**Em FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} configurar política de negociação mm**  

1.  Adicione um ou ambos os seguintes contextos do provedor de política MM.  
    -   Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT.
    -   Para a AuthIP, um contexto de provedor de política do tipo FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política mm correspondente será aplicada. AuthIP é o módulo de chave preferencial se há suporte para IKE e AuthIP.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.

    | Propriedade Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor MM adicionado na etapa 1. |

        

**Em FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} configurar política de negociação de QM e EM**  

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e de definido o sinalizador [**\_ \_ \_ ND \_ SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) do SINALIZADOR DE POLÍTICA IPSEC.  
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

    | Propriedade Filter                                               | Valor                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | Condição de filtragem DE TIPO DE \_ \_ ENDEREÇO LOCAL IP \_ DA \_ \_ CONDIÇÃO DO FWPM | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                               | **TERMINAÇÃO DO \_ \_ CALLOUT DA AÇÃO FWP \_**                                                              |
    | **action.calloutKey**                                         | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**                                              |
    | **rawContext**                                                | [**SEGURANÇA DE CONEXÃO DE PERSISTÊNCIA DE \_ \_ IPSEC \_ DE \_ \_ \_ CONTEXTO DO FWPM**](filter-context-identifiers.md) |

        
2.  Isente o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de \_ \_ filtragem CONDITION IP PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Essas constantes são definidas em winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISSÃO DE AÇÃO \_ FWP \_**                                                    |
    | **weight**                                                        | [**ISENÇÕES DE IKE DO INTERVALO DE PESO DO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**Em FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} configure regras de filtragem de saída por pacote**  

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
    | **FWPM \_ Condição de \_ filtragem CONDITION IP \_ LOCAL \_ ADDRESS \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**                                   |

        
3.  Adicione um filtro com as propriedades a seguir. Esse filtro só permitirá conexões de entrada para a porta TCP 5555 se elas forem criptografadas.

    | Propriedade de filtro                                                   | Valor                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                                           |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ TCP** essa constante é definida no Winsock2. h.<br/>                                    |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**          | 5555                                                                                                  |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                                                                 |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**                                          |
    | **rawContext**                                                    | [**\_conexão do conjunto de Ale de contexto FWPM \_ \_ \_ \_ requer \_ \_ criptografia IPSec**](filter-context-identifiers.md) |

        

**No FWPM \_ Layer \_ Ale \_ auth \_ Connect \_ V {4 \| 6} configurar as regras de filtragem por conexão de saída**

-   Adicione um filtro com as propriedades a seguir. Esse filtro só permitirá conexões de saída da porta TCP 5555 se elas forem criptografadas.

    | Propriedade de filtro                                                   | Valor                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                                           |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ TCP** essa constante é definida no Winsock2. h.<br/>                                    |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**          | 5555                                                                                                  |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                                                                 |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec \_ Ale \_ Connect \_ V {4 \| 6}**                                                       |
    | **rawContext**                                                    | [**\_conexão do conjunto de Ale de contexto FWPM \_ \_ \_ \_ requer \_ \_ criptografia IPSec**](filter-context-identifiers.md) |

      

  
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

 

