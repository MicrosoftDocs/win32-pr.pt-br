---
description: Referência de consulta COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referência de consulta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010065"
---
# <a name="copp-query-reference"></a>Referência de consulta COPP

Esta seção descreve as consultas de status com suporte pelo protocolo de proteção de saída certificado (COPP). Para cada consulta, o GUID que define a consulta é listado, junto com os dados de entrada e retorna dados.



| Consulta                   | GUID                                     |
|-------------------------|------------------------------------------|
| Dados de barramento                | **COPPQueryBusData de DXVA \_**               |
| Tipo de Conector          | **COPPQueryConnectorType de DXVA \_**         |
| Exibir dados            | **COPPQueryDisplayData de DXVA \_**           |
| Dados de chave de HDCP           | **COPPQueryHDCPKeyData de DXVA \_**           |
| Nível de proteção global | **COPPQueryGlobalProtectionLevel de DXVA \_** |
| Nível de proteção local  | **COPPQueryLocalProtectionLevel de DXVA \_**  |
| Tipo de proteção         | **COPPQueryProtectionType de DXVA \_**        |
| Sinalização               | **COPPQuerySignaling de DXVA \_**             |



 

Consulta de dados de barramento

Retorna o tipo de barramento de e/s usado pelo adaptador de gráficos.

-   **GUID**: DXVA \_ COPPQueryBusData
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . O tipo de barramento é retornado no membro **dwData** como um sinalizador da enumeração [**de \_ BusType Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .

Consulta de tipo de conector

Retorna o tipo de conector físico.

-   **GUID**: DXVA \_ COPPQueryConnectorType
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . O tipo de conector é retornado no membro **dwData** como um sinalizador da enumeração do tipo de [**\_ conector Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .

Consulta de exibição de dados

Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.

O sinal de vídeo transmitido pelo conector não necessariamente tem o mesmo formato que o modo de exibição da área de trabalho. Por exemplo, o modo de exibição de área de trabalho pode ser de 1024x768 pixels a 85 Hz, enquanto o conector pode ser um conector de S-video que transmite um sinal de vídeo em 720x480 pixels, 60/1.01 Hz entrelaçados. Nesse caso, o driver retornaria a resolução do sinal S-Video, não a resolução da área de trabalho.

-   **GUID**: DXVA \_ COPPQueryDisplayData
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusDisplayData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .

Consulta de dados de chave de HDCP

Retorna o vetor de seleção de chave de HDCP do dispositivo (B-KSV).

O KSV é um identificador fornecido para o fabricante do dispositivo e é usado no processo de autenticação e configuração de HDCP. O aplicativo deve verificar esse valor em relação à lista de KSVs revogados. O mecanismo para obter a lista de revogação de KSV está fora do escopo do protocolo COPP. Para obter mais informações, consulte a especificação de HDCP.

Essa consulta também determina se o dispositivo HDCP conectado é um monitor ou um repetidor HDCP. O aplicativo não deve reproduzir conteúdo protegido se o dispositivo HDCP for um repetidor HDCP, porque eles não têm suporte de COPP.

-   **GUID**: DXVA \_ COPPQueryHDCPKeyData
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusHDCPKeyData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .

Consulta de nível de proteção global

Retorna o nível de proteção global para um mecanismo de proteção especificado.

O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver de gráficos foi instruído a aplicar a proteção. Por exemplo, um aplicativo pode definir o nível de proteção de ACP chamando a função **ChangeDisplaySettingsEx** . Nesse caso, o nível de proteção global refletiria essa configuração, embora não tenha sido solicitada por meio de COPP.

-   **GUID**: DXVA \_ COPPQueryGlobalProtectionLevel
-   **Dados de entrada**: o mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md).
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . O nível de proteção atual é retornado no membro **dwData** . O significado desse valor depende do mecanismo de proteção que é consultado. Para cada mecanismo de proteção, o valor do membro **dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.

    | Mecanismo de proteção | Enumeração                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**\_Nível de \_ proteção de ACP de Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Nível de \_ proteção Copp CGMSA \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Nível de \_ proteção de HDCP de Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de nível de proteção local

Retorna o nível de proteção local para um mecanismo de proteção especificado.

O nível de proteção local é o nível de proteção que foi solicitado por meio da sessão COPP atual. O driver pode definir um nível de proteção mais alto.

-   **GUID**: DXVA \_ COPPQueryLocalProtectionLevel
-   **Dados de entrada**: o mecanismo de proteção a ser consultado como um inteiro de 32 bits. Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md).
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . O nível de proteção atual é retornado no membro **dwData** . O significado desse valor depende do mecanismo de proteção que é consultado. Para cada mecanismo de proteção, o valor do membro **dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.

    | Mecanismo de proteção | Enumeração                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**\_Nível de \_ proteção de ACP de Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Nível de \_ proteção Copp CGMSA \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Nível de \_ proteção de HDCP de Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de tipo de proteção

Retorna os mecanismos de proteção disponíveis para o conector.

-   **GUID**: DXVA \_ COPPQueryProtectionType
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Os mecanismos de proteção são retornados no membro **dwData** como uma combinação de zero ou mais sinalizadores. Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md). Se mais de um mecanismo de proteção estiver disponível, os sinalizadores serão combinados com um **OR bit a** bit.

Consulta de sinalização

Retorna uma lista de todos os padrões de proteção compatíveis com o driver, o padrão atualmente ativo e a taxa de proporção atual ou outros dados de sinalização.

-   **GUID**: DXVA \_ COPPQuerySignaling
-   **Dados de entrada**: nenhum.
-   **Retornar dados**: retorna uma estrutura de [**\_ COPPStatusSignalingCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



