---
description: Retorna o nível de proteção virtual para um mecanismo de proteção especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813334"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ obter \_ \_ nível de proteção virtual \_

Retorna o nível de proteção virtual para um mecanismo de proteção especificado.

O nível de proteção *virtual* é o nível solicitado pelo aplicativo durante a sessão do Gerenciador de proteção de saída (OPM) atual. O driver pode aplicar um nível mais alto, devido a eventos fora dessa sessão OPM. Para localizar o nível de proteção real que está em vigor, envie a consulta de [**\_ \_ \_ \_ nível de proteção OPM**](opm-get-actual-protection-level.md) .



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | OPM \_ obter \_ \_ nível de proteção virtual \_                                                                                                                                          |
| Dados de entrada   | O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. O valor é interpretado como um membro dos [**sinalizadores de tipo de proteção OPM**](opm-protection-type-flags.md). |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Comentários

O nível de proteção é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O significado desse valor depende do mecanismo de proteção que é consultado. Para cada mecanismo de proteção, o valor de **ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.



| Mecanismo de proteção | Enumeração                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**nível de proteção do OPM \_ ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**CGMS-um sinalizador de proteção**](cgms-a-protection-flags.md)        |
| DPCP                 | [**\_nível de \_ proteção OPM DPCP \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**\_nível de \_ proteção de HDCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Essa consulta é equivalente à consulta DXVA \_ COPPQueryLocalProtectionLevel usada no protocolo de proteção de saída certificado (Copp).

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

 

 




