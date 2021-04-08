---
description: Retorna o nível de proteção global para um mecanismo de proteção especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010663"
---
# <a name="opm_get_actual_protection_level"></a>nível de proteção do OPM \_ obter \_ real \_ \_

Retorna o nível de proteção global para um mecanismo de proteção especificado.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | nível de proteção do OPM \_ obter \_ real \_ \_                                                                                                                                       |
| Dados de entrada   | O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. O valor é interpretado como um membro dos [sinalizadores de tipo de proteção OPM](opm-protection-type-flags.md). |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Comentários

O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver de gráficos foi instruído a aplicar a proteção. Por exemplo, um aplicativo pode definir o nível de proteção de ACP chamando a função **ChangeDisplaySettingsEx** . Nesse caso, o nível de proteção global refletiria essa configuração, embora ela não tenha sido solicitada por meio do Gerenciador de proteção de saída (OPM).

O nível de proteção é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O significado desse valor depende do mecanismo de proteção que é consultado. Para cada mecanismo de proteção, o valor de **ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.



| Mecanismo de proteção | Enumeração                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**nível de proteção do OPM \_ ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [CGMS-um sinalizador de proteção](cgms-a-protection-flags.md)            |
| DPCP                 | [**\_nível de \_ proteção OPM DPCP \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**\_nível de \_ proteção de HDCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Essa consulta é equivalente à consulta DXVA \_ COPPQueryGlobalProtectionLevel usada no protocolo de proteção de saída certificado (Copp).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitações de status OPM](opm-status-requests.md)
</dt> </dl>

 

 




