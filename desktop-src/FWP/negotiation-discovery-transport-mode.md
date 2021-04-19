---
title: Modo de transporte de descoberta de negociação
description: O cenário de política IPsec do modo de transporte da descoberta de negociação requer a proteção do modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita a proteção de IPsec para correspondência do tráfego de saída.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314809"
---
# <a name="negotiation-discovery-transport-mode"></a>Modo de transporte de descoberta de negociação

O cenário de política IPsec do modo de transporte da descoberta de negociação requer a proteção do modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita a proteção de IPsec para correspondência do tráfego de saída. Portanto, as conexões de saída têm permissão para fazer fallback para texto não criptografado enquanto as conexões de entrada não são.

Com essa política, quando o computador host tenta uma nova conexão de saída e não há nenhuma SA IPsec existente que corresponda ao tráfego, o host envia simultaneamente os pacotes em texto não criptografado e inicia uma negociação IKE ou AuthIP. Se a negociação for realizada com sucesso, a conexão será atualizada para protegido por IPsec. Caso contrário, a conexão permanecerá em texto não criptografado. Depois de protegida por IPsec, uma conexão nunca pode ser rebaixada para texto não criptografado.

O modo de transporte de descoberta de negociação normalmente é usado em ambientes que incluem máquinas compatíveis com IPsec e não com IPsec.

Um exemplo de cenário de modo de transporte de descoberta de negociação é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec e habilitar a descoberta de negociação".

Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.

<dl>

**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} configurar a política de negociação mm**  

1.  Adicione um ou ambos os seguintes contextos do provedor de política MM.  
    -   Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ Ike \_ mm \_ Context**.
    -   Para AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política MM correspondente será aplicada. AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir. 

    | Propriedade de filtro        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor MM adicionado na etapa 1. |

        

**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**  

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador [**\_ \_ \_ \_ seguro do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_ .
    -   Para AuthIP, um contexto de provedor de política do \_ tipo \_ \_ contexto de transporte QM IPSec AuthIP de FWPM \_ \_ . Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).

    > [!Note]  
    > Um módulo de chave comum será negociado e a política QM correspondente será aplicada. AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir. 

    | Propriedade de filtro        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto de provedor QM adicionado na etapa 1. |

        

**No \_ transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**  

1.  Adicione um filtro com as propriedades a seguir. 

    | Propriedade de filtro                                                   | Valor                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                                                              |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                    | [**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**](filter-context-identifiers.md) |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | [**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**](filter-weight-identifiers.md)  |

        

**No transporte de saída da camada do FWPM \_ \_ \_ \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**  

1.  Adicione um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                               |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                                                     |
    | **ação. calloutKey**                                             | **FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**                                    |
    | **rawContext**                                                    | [**\_descoberta de \_ \_ negociação de saída IPSec de contexto \_ FWPM \_**](filter-context-identifiers.md) |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**                                   |

        

**Na camada FWPM de \_ \_ autenticação Ale, \_ \_ \_ aceite \_ V {4 \| 6} configurar regras de filtragem de entrada por conexão**  

1.  Adicione um filtro com as propriedades a seguir. Esse filtro só permitirá tentativas de conexão de entrada se elas forem protegidas pelo IPsec. 

    | Propriedade de filtro                                                   | Valor                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                  |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                        |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}** |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                                                      |
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

 

