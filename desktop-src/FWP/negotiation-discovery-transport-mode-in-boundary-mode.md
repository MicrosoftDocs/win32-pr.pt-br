---
title: Modo de transporte de descoberta de negociação no modo de limite
description: O modo de transporte da descoberta de negociação no modo de limite cenário de política IPsec solicita a proteção do modo de transporte IPsec para todo o tráfego correspondente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9f4168eee38165125c2455bc80dae29c1c6794
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454056"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a>Modo de transporte de descoberta de negociação no modo de limite

O modo de transporte da descoberta de negociação no modo de limite cenário de política IPsec solicita a proteção do modo de transporte IPsec para todo o tráfego correspondente. Se a negociação IKE/AuthIP falhar, as conexões de entrada e saída terão permissão para fazer fallback para o texto não criptografado.

Essa diretiva IPsec é normalmente usada em computadores que são acessados por máquinas compatíveis com IPsec e não com IPsec.

Um exemplo de cenário de modo de transporte de descoberta de negociação potencial é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec e habilitar a descoberta de negociação no modo de limite".

Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.

<dl>

**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**  

1.  Adicione um ou ambos os seguintes contextos do provedor de política MM.  
    -   Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSec \_ Ike \_ mm \_ Context.
    -   Para AuthIP, um contexto de provedor de política do tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.

    > [!Note]  
    > Um módulo de chave comum será negociado e a política MM correspondente será aplicada. AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.
    | Propriedade de filtro        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto do provedor MM adicionado na etapa 1. |

        

**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**  

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador de [**\_ \_ \_ \_ limite do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.
    -   Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM**. Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).

    > [!Note]  
    > Um módulo de chave comum será negociado e a política QM correspondente será aplicada. AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.

     

2.  Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.
    | Propriedade de filtro        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condições de filtragem   | Vazio. Todo o tráfego corresponderá ao filtro.        |
    | **providerContextKey** | GUID do contexto de provedor QM adicionado na etapa 1. |

        

**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**  

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
    | **ação. tipo**                                                   | \_permissão de ação fwp \_                                                        |
    | **weight**                                                        | [**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**](filter-weight-identifiers.md)  |

        

**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**  

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

        

</dl>

> [!Note]  
> Em oposição ao modo de transporte de descoberta de negociação, para o modo de transporte de descoberta de negociação na política de modo de limite, não há necessidade de adicionar um filtro nas camadas de **\_ recebimento de autenticação Ale de camada FWPM \_ \_ \_ \_ \_ V {4 \| 6}** , pois essa política permite conexões de texto não criptografado de entrada não protegidas.

 

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

 

