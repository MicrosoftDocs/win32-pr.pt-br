---
description: Referência de consulta COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referência de consulta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d36cde152600faaa1dd567faac916bfa8281e2b2edb9464074fe34a58d5011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909656"
---
# <a name="copp-query-reference"></a>Referência de consulta COPP

Esta seção descreve as consultas de status com suporte pelo COPP (Certified Output Protection Protocol). Para cada consulta, o GUID que define a consulta é listado, juntamente com os dados de entrada e os dados de retorno.



| Consulta                   | GUID                                     |
|-------------------------|------------------------------------------|
| Dados do Barramento                | **DXVA \_ COPPQueryBusData**               |
| Tipo de Conector          | **DXVA \_ COPPQueryConnectorType**         |
| Exibir dados            | **DXVA \_ COPPQueryDisplayData**           |
| Dados de chave HDCP           | **DXVA \_ COPPQueryHDCPKeyData**           |
| Nível de proteção global | **DXVA \_ COPPQueryGlobalProtectionLevel** |
| Nível de proteção local  | **DXVA \_ COPPQueryLocalProtectionLevel**  |
| Tipo de proteção         | **DXVA \_ COPPQueryProtectionType**        |
| Sinalização               | **DXVA \_ COPPQuerySignaling**             |



 

Consulta de dados do barramento

Retorna o tipo de barramento de E/S usado pelo adaptador de gráficos.

-   **GUID:** DXVA \_ COPPQueryBusData
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) O tipo de barramento é retornado no **membro dwData** como um sinalizador da [**enumeração \_ BusType copp.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype)

Consulta de tipo de conector

Retorna o tipo de conector físico.

-   **GUID:** DXVA \_ COPPQueryConnectorType
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) O tipo de conector é retornado no **membro dwData** como um sinalizador da [**enumeração COPP \_ ConnectorType.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype)

Exibir consulta de dados

Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.

O sinal de vídeo transmitido pelo conector não tem necessariamente o mesmo formato que o modo de exibição da área de trabalho. Por exemplo, o modo de exibição da área de trabalho pode ter 1024 x 768 pixels a 85 Hz, enquanto o conector pode ser um conector S-Video que transmite um sinal de vídeo a 720 x 480 pixels, entrelaçados de 60/1,01 Hz. Nesse caso, o driver retornaria a resolução do sinal S-Video, não a resolução da área de trabalho.

-   **GUID:** DXVA \_ COPPQueryDisplayData
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusDisplayData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata)

Consulta de dados de chave HDCP

Retorna o vetor de seleção de chave HDCP do dispositivo (B-KSV).

O KSV é um identificador fornecido ao fabricante do dispositivo e é usado no processo de configuração e autenticação do HDCP. O aplicativo deve verificar esse valor em relação à lista de KSVs revogados. O mecanismo para obter a lista de revogação de KSV está fora do escopo do protocolo COPP. Para obter mais informações, consulte a especificação do HDCP.

Essa consulta também determina se o dispositivo HDCP conectado é um monitor ou um repetidor HDCP. O aplicativo não deverá reproduzir conteúdo protegido se o dispositivo HDCP for um repetidor HDCP, pois eles não têm suporte do COPP.

-   **GUID:** DXVA \_ COPPQueryHDCPKeyData
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusHDCPKeyData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata)

Consulta de nível de proteção global

Retorna o nível de proteção global para um mecanismo de proteção especificado.

O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver gráfico foi instruído a aplicar a proteção. Por exemplo, um aplicativo pode definir o nível de proteção ACP chamando a **função ChangeDisplaySettingsEx.** Nesse caso, o nível de proteção global refletiria essa configuração, mesmo que ela não fosse solicitada por meio do COPP.

-   **GUID:** DXVA \_ COPPQueryGlobalProtectionLevel
-   **Dados de** entrada: o mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. Consulte [Sinalizadores de tipo de proteção COPP](copp-protection-type-flags.md).
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) O nível de proteção atual é retornado no **membro dwData.** O significado desse valor depende do mecanismo de proteção consultado. Para cada mecanismo de proteção, o valor do **membro dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.

    | Mecanismo de proteção | Enumeração                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nível de proteção \_ do COPP \_ \_ ACP**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nível de \_ proteção do COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Nível de proteção \_ DO HDCP \_ do COPP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta no nível de proteção local

Retorna o nível de proteção local para um mecanismo de proteção especificado.

O nível de proteção local é o nível de proteção que foi solicitado por meio da sessão copp atual. O driver pode definir um nível de proteção mais alto.

-   **GUID:** DXVA \_ COPPQueryLocalProtectionLevel
-   **Dados de** entrada: o mecanismo de proteção a ser consultado, como um inteiro de 32 bits. Consulte [Sinalizadores de tipo de proteção COPP](copp-protection-type-flags.md).
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) O nível de proteção atual é retornado no **membro dwData.** O significado desse valor depende do mecanismo de proteção consultado. Para cada mecanismo de proteção, o valor do **membro dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.

    | Mecanismo de proteção | Enumeração                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nível de proteção \_ do COPP \_ \_ ACP**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nível de \_ proteção do COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Nível de proteção \_ DO HDCP \_ do COPP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de tipo de proteção

Retorna os mecanismos de proteção que estão disponíveis para o conector.

-   **GUID:** DXVA \_ COPPQueryProtectionType
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma estrutura [**\_ COPPStatusData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Os mecanismos de proteção são retornados no **membro dwData** como uma combinação de zero ou mais sinalizadores. Consulte [Sinalizadores de tipo de proteção COPP](copp-protection-type-flags.md). Se mais de um mecanismo de proteção estiver disponível, os sinalizadores serão combinados com um OR bit a **bit.**

Consulta de sinalização

Retorna uma lista de todos os padrões de proteção com suporte pelo driver, o padrão que está ativo no momento e a taxa de proporção atual ou outros dados de sinalização.

-   **GUID:** DXVA \_ COPPQuerySignaling
-   **Dados de entrada:** nenhum.
-   **Retornar dados:** retorna uma [**estrutura \_ COPPStatusSignalingCmdData DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



