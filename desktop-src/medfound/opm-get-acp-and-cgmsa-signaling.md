---
description: 'Saiba mais sobre: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102060"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling

Retorna as seguintes informações sobre uma saída de vídeo:

-   Uma lista de padrões de proteção de televisão com suporte pelo driver.
-   O padrão que está ativo no momento.
-   A taxa de proporção atual ou outros dados de sinalização.



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------|
| GUID de solicitação | os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling                                                |
| Dados de entrada   | Nenhum                                                                                |
| Retornar dados  | Uma estrutura de [**\_ \_ \_ \_ sinalização de erro OPM e CGMSA**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Comentários

Essa consulta é equivalente à consulta DXVA \_ COPPQuerySignaling usada no protocolo de proteção de saída certificado (Copp).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitações de status OPM](opm-status-requests.md)
</dt> </dl>

 

 




