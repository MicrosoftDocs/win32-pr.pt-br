---
title: Modo de transporte
description: O cenário de política IPsec do modo de transporte requer a proteção do modo de transporte IPsec para todo o tráfego correspondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314929"
---
# <a name="transport-mode"></a>Modo de transporte

O cenário de política IPsec do modo de transporte requer a proteção do modo de transporte IPsec para todo o tráfego correspondente. Qualquer tráfego de texto não criptografado correspondente é Descartado até que a negociação IKE ou AuthIP seja concluída com êxito. Se a negociação falhar, a conectividade com o endereço IP correspondente permanecerá quebrada.

Um exemplo de um possível cenário de modo de transporte é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec".

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

1.  Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM.  
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

    | Propriedade de filtro                                                   | Valor                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **ação. tipo**                                                   | o \_ \_ texto explicativo de ação fwp \_ termina                             |
    | **ação. calloutKey**                                             | FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}             |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                  | Valor                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                               |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**            | IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.<br/>    |
    | **ação. tipo**                                                  | \_permissão de ação fwp \_                                                       |
    | **weight**                                                       | [**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**](filter-weight-identifiers.md) |

        

**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**  

1.  Adicione um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                        |
    | **ação. tipo**                                                   | **o \_ \_ texto explicativo de ação fwp \_ termina**              |
    | **ação. calloutKey**                                             | FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6} |

        
2.  Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.

    | Propriedade de filtro                                                   | Valor                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição** | NlatUnicast                                                            |
    | **FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**             | IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.<br/> |
    | **ação. tipo**                                                   | \_permissão de ação fwp \_                                                    |
    | **weight**                                                        | \_ \_ isenções Ike de intervalo de peso FWPM \_ \_                                   |

        

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

[**Identificadores de texto explicativo internos**](built-in-callout-identifiers.md)
</dt> </dl>

 

