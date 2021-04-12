---
description: Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296533"
---
# <a name="opm_get_actual_output_format"></a>formato de saída de OPM de \_ obtenção \_ real \_ \_

Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.



| Requisito | Valor |
|--------------|------------------------------------------------------------------------------|
| GUID de solicitação | formato de saída de OPM de \_ obtenção \_ real \_ \_                                             |
| Dados de entrada   | Nenhum                                                                         |
| Retornar dados  | Uma estrutura de [**\_ formato de \_ saída \_ de OPM real**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Comentários

O sinal de vídeo transmitido pelo conector não necessariamente tem o mesmo formato que o modo de exibição da área de trabalho. Por exemplo, o modo de exibição de área de trabalho pode ser 1024 x 768 pixels às 85 Hz, enquanto o conector pode ser um conector de S-video que transmite um sinal de vídeo em 720 x 480 pixels, 60/1.01 Hz entrelaçado. Nesse caso, o driver retornaria a resolução do sinal S-Video, não a resolução da área de trabalho.

Essa consulta é equivalente à consulta DXVA \_ COPPQueryDisplayData usada no protocolo de proteção de saída certificado (Copp).

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

 

 




