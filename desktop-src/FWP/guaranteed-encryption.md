---
title: Criptografia garantida
description: O cenário de política IPsec de criptografia garantida requer criptografia IPsec para todo o tráfego correspondente. Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120e9cb794b6010e16dd5f61accb07ca0ab9cb8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365965"
---
# <a name="guaranteed-encryption"></a>Criptografia garantida

O cenário de política IPsec de criptografia garantida requer criptografia IPsec para todo o tráfego correspondente. Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.

A criptografia garantida normalmente é usada para criptografar o tráfego confidencial por aplicativo.

Um exemplo de um possível cenário de criptografia garantida é "proteger todo o tráfego de dados unicast, exceto ICMP, usar o modo de transporte IPsec, habilitar a descoberta de negociação e exigir a criptografia garantida para todo o tráfego unicast correspondente à porta local TCP 5555".

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

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador [**\_ \_ \_ \_ seguro do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
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
    | Propriedade de filtro                                               | Valor                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | \_Condição de \_ filtragem \_ de \_ tipo de endereço local IP de condição FWPM \_ | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **ação. tipo**                                               | **o \_ \_ texto explicativo de ação fwp \_ termina**                                                              |
    | **ação. calloutKey**                                         | **FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                | [**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**](filter-context-identifiers.md) |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.
    | Propriedade de filtro                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                                |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | **IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | **\_permissão de ação fwp \_**                                                    |
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

 

