---
description: Os sinalizadores na tabela a seguir especificam mecanismos de proteção de saída para o Gerenciador de proteção de saída (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Sinalizadores de tipo de proteção OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ee61b17ee1708f8c2fc7e2f91b33d966b17f8fd2e198e2772c30ccccf837d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101885"
---
# <a name="opm-protection-type-flags"></a>Sinalizadores de tipo de proteção OPM

Os sinalizadores na tabela a seguir especificam mecanismos de proteção de saída para o Gerenciador de proteção de saída (OPM).



| Constante/valor                                                                                                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ Tipo de proteção \_ \_ outro**</dt> <dt>0x80000000</dt> </dl>                                                | Mecanismo de proteção desconhecido.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ Tipo de proteção \_ \_ nenhum**</dt> <dt>0x00000000</dt> </dl>                                                   | Nenhum mecanismo de proteção.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ Tipo de proteção de \_ \_ \_ \_ HDCP compatível com a Copp**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth Proteção de Conteúdo Digital (HDCP). Esse sinalizador é usado ao emular o protocolo de proteção de saída certificado (COPP). Para obter mais informações, consulte Comentários. Esse sinalizador não tem suporte para semântica OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ Tipo de proteção \_ \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Proteção de cópia analógica (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ Tipo de proteção \_ \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Sistema de gerenciamento de geração de cópia — analógico (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ Tipo de proteção de \_ \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | HDCP. Esse sinalizador é usado quando o objeto OPM tem semântica OPM. Não há suporte para semântica COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ Tipo de proteção \_ \_ DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | Proteção de Conteúdo DisplayPort (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Comentários

Esses sinalizadores são usados nos seguintes comandos de OPM e solicitações de status.

-   [OPM \_ definir \_ nível de proteção \_](opm-set-protection-level.md)
-   [OPM \_ obter \_ \_ nível de proteção virtual \_](opm-get-virtual-protection-level.md)
-   [nível de proteção do OPM \_ obter \_ real \_ \_](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>HDCP

Os dois sinalizadores a seguir são definidos para HDCP.



| Valor                                         | Descrição                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tipo de proteção OPM de \_ \_ \_ HDCP                   | Use esse sinalizador se o ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) tiver sido criado com semântica OPM.                                                                        |
| tipo de proteção OPM de \_ \_ \_ \_ HDCP compatível com Copp \_ | Use esse sinalizador se o ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) tiver sido criado com semântica COPP. Esse sinalizador corresponde ao sinalizador de \_ HDCP de proteção de Copp \_ em COPP. |



 

Ambos os modos (semântica de OPM e semânticos de COPP) dão suporte às seguintes operações para HDCP:

-   Habilitar ou desabilitar o HDCP usando o comando de [nível de proteção de OPM \_ set \_ Protection \_ ](opm-set-protection-level.md) .
-   Consulte se a HDCP está habilitada usando a solicitação de status de [nível de \_ \_ \_ proteção \_ ](opm-get-actual-protection-level.md) do [OPM \_ \_ \_ \_ ](opm-get-virtual-protection-level.md)

A semântica de OPM também oferece suporte ao seguinte:

-   Repetidores de HDCP. Um *repetidor HDCP* é um dispositivo HDCP que pode receber conteúdo HDCP e também criptografar novamente e transmitir o mesmo conteúdo.
-   Revogação de HDCP. Se um dispositivo HDCP revogado for anexado à saída de vídeo OPM, a saída de vídeo não transmitirá o vídeo. O aplicativo não precisa analisar SRMs (mensagens de renovação do sistema HDCP) ou determinar se o dispositivo de saída foi revogado. Para obter mais informações, consulte o comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Quando a semântica COPP é usada, a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) não dá suporte a repetidores de HDCP. Além disso, ele não trata a revogação de HDCP. Em vez disso, o aplicativo deve analisar o SRM para determinar se um dispositivo HDCP foi revogado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de OPM](opm-enumerations.md)
</dt> </dl>

 

 




