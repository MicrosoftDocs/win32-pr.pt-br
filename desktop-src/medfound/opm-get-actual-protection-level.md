---
description: Retorna o nível de proteção global para um mecanismo de proteção especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5d895c037fedfa97bbafab8331d685af9a7f1ce81489b8d600bd903aa2a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101915"
---
# <a name="opm_get_actual_protection_level"></a>OBTER NÍVEL DE \_ \_ PROTEÇÃO REAL DO \_ OPM \_

Retorna o nível de proteção global para um mecanismo de proteção especificado.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | OBTER NÍVEL DE \_ \_ PROTEÇÃO REAL DO \_ OPM \_                                                                                                                                       |
| Dados de entrada   | O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits. O valor é interpretado como um membro dos Sinalizadores de Tipo de Proteção [do OPM.](opm-protection-type-flags.md) |
| Retornar dados  | Uma [**estrutura de INFORMAÇÕES PADRÃO \_ \_ do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Comentários

O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver gráfico foi instruído a aplicar a proteção. Por exemplo, um aplicativo pode definir o nível de proteção ACP chamando a **função ChangeDisplaySettingsEx.** Nesse caso, o nível de proteção global refletiria essa configuração, mesmo que ela não fosse solicitada por meio do OPM (Gerenciador de Proteção de Saída).

O nível de proteção é retornado no **membro ulInformation** da estrutura [**OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) O significado desse valor depende do mecanismo de proteção consultado. Para cada mecanismo de proteção, o valor **de ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.



| Mecanismo de proteção | Enumeração                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**NÍVEL DE PROTEÇÃO ACP DO OPM \_ \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [Sinalizadores de proteção do CGMS-A](cgms-a-protection-flags.md)            |
| DPCP                 | [**NÍVEL DE \_ PROTEÇÃO DPCP \_ DO OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**NÍVEL DE \_ PROTEÇÃO HDCP \_ DO OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Essa consulta é equivalente à consulta \_ COPPQueryGlobalProtectionLevel DXVA usada no COPP (Certified Output Protection Protocol).

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

 

 




