---
title: Autorização de identidade remota
description: O cenário da política IPsec de autorização de identidade remota requer que as conexões de entrada venham de um conjunto específico de entidades de segurança remotas que são especificadas em uma ACL (lista de controle de acesso) do Windows Security Descriptor (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314829"
---
# <a name="remote-identity-authorization"></a>Autorização de identidade remota

O cenário da política IPsec de autorização de identidade remota requer que as conexões de entrada venham de um conjunto específico de entidades de segurança remotas que são especificadas em uma ACL (lista de controle de acesso) do Windows Security Descriptor (SD). Se a identidade remota (conforme determinado pelo IPsec) não corresponder ao conjunto de identidades permitidas, a conexão será descartada. Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.

Se o AuthIP estiver habilitado, dois descritores de segurança poderão ser especificados, um correspondente ao modo principal de AuthIP e o outro correspondente ao modo estendido AuthIP.

Um exemplo de cenário de modo de transporte de descoberta de negociação é "proteger todos os tráfegos de dados unicast, exceto ICMP, usando o modo de transporte IPsec, habilitar a descoberta de negociação e restringir o acesso de entrada a identidades remotas permitidas de acordo com o modo estendido do AuthIP), para todo o tráfego unicast correspondente à porta TCP local 5555."

Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.

<dl>

**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**  

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
    -   Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.
    -   Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM** que contém a política de negociação em modo estendido AuthIP.

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

    | Propriedade de filtro                                                   | Valor                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                            |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                |
    | **weight**                                                        | **\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**                               |

        

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

        
3.  Adicione um filtro com as propriedades a seguir. Esse filtro permitirá conexões de entrada para a porta TCP 5555 se as identidades remotas correspondentes forem permitidas por SD1 e SD2. 

    | Propriedade de filtro                                                   | Valor                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                        |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ TCP** essa constante é definida no Winsock2. h.<br/> |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**          | 5555                                                               |
    | **\_ID da \_ \_ máquina remota \_ Ale \_ da condição FWPM**                     | SD1                                                                |
    | **\_ID de \_ \_ usuário remoto \_ Ale \_ da condição FWPM**                        | SD2                                                                |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**                              |
    | **ação. calloutKey**                                             | **FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**       |

        
4.  Adicione um filtro com as propriedades a seguir. Esse filtro bloqueará quaisquer outras conexões de entrada para a porta TCP 5555 que não correspondam ao filtro anterior. 

    | Propriedade de filtro                                                   | Valor                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                        |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ TCP** essa constante é definida no Winsock2. h.<br/> |
    | **FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**          | 5555                                                               |
    | **ação. tipo**                                                   | **\_bloco de ação fwp \_**                                             |

        

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

 

