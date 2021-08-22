---
description: Retorna o nível de proteção virtual para um mecanismo de proteção especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fb4130b4ad700de2328114dbf900ff7d122045b277c8a5ae812332c730a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972915"
---
# <a name="opm_get_virtual_protection_level"></a>OBTER NÍVEL DE \_ \_ PROTEÇÃO VIRTUAL \_ DO OPM \_

Retorna o nível de proteção virtual para um mecanismo de proteção especificado.

O nível de proteção *virtual* é o nível solicitado pelo aplicativo durante a sessão atual do OPM (Gerenciador de Proteção de Saída). O driver pode aplicar um nível mais alto, devido a eventos fora dessa sessão do OPM. Para encontrar o nível de proteção real que está em vigor, envie a consulta [**GET ACTUAL PROTECTION LEVEL \_ \_ \_ \_ do OPM.**](opm-get-actual-protection-level.md)



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | OBTER NÍVEL DE \_ \_ PROTEÇÃO VIRTUAL \_ DO OPM \_                                                                                                                                          |
| Dados de entrada   | O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. O valor é interpretado como um membro dos Sinalizadores de Tipo de Proteção [**do OPM.**](opm-protection-type-flags.md) |
| Retornar dados  | Uma [**estrutura de INFORMAÇÕES PADRÃO \_ \_ do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Comentários

O nível de proteção é retornado no **membro ulInformation** da estrutura [**OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) O significado desse valor depende do mecanismo de proteção consultado. Para cada mecanismo de proteção, o valor **de ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.



| Mecanismo de proteção | Enumeração                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**NÍVEL DE PROTEÇÃO ACP DO OPM \_ \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**Sinalizadores de proteção do CGMS-A**](cgms-a-protection-flags.md)        |
| DPCP                 | [**NÍVEL DE \_ PROTEÇÃO DPCP \_ DO OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**NÍVEL DE \_ PROTEÇÃO HDCP \_ DO OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Essa consulta é equivalente à consulta \_ COPPQueryLocalProtectionLevel DXVA usada no COPP (Certified Output Protection Protocol).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitações de status do OPM](opm-status-requests.md)
</dt> </dl>

 

 




