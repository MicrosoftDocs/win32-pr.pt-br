---
description: 'Saiba mais sobre: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d692680e6492a3dc5d92073baf069eefffde68841925ced9afd69dde4d5fcd97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239889"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OBTER INFORMAÇÕES DE \_ \_ DISPOSITIVO \_ HDCP \_ \_ CONECTADAS DO OPM

Obtém informações sobre um High-Bandwidth HDCP (Proteção de Conteúdo digital) anexado à saída de vídeo. As seguintes informações são retornadas:

-   O KSV (vetor de seleção de chave HDCP) do dispositivo.
-   Se o dispositivo é um repetidor HDCP.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID de solicitação | OBTER INFORMAÇÕES DE \_ \_ DISPOSITIVO \_ HDCP \_ \_ CONECTADAS DO OPM                                                          |
| Dados de entrada   | Nenhum                                                                                                    |
| Retornar dados  | Uma [**estrutura de INFORMAÇÕES DO DISPOSITIVO \_ \_ HDCP CONECTADO \_ \_ DO OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Comentários

Essa consulta só pode ser usada com o modo *de emulação COPP*. Se a [**interface IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usar a semântica do OPM (Gerenciador de Proteção de Saída), não há suporte para essa solicitação de status.

O KSV é um identificador fornecido ao fabricante do dispositivo e é usado no processo de configuração e autenticação do HDCP. No modo de emulação COPP, o aplicativo usa o KSV para determinar se o dispositivo HDCP é revogado. Se for, o aplicativo não deve reproduzir conteúdo protegido. Além disso, o aplicativo não deve reproduzir conteúdo protegido se o dispositivo for um repetidor HDCP, pois o COPP não dá suporte a repetidores HDCP.

Essa consulta não é necessária quando a semântica do OPM é usada, pois o OPM dá suporte à revogação de dispositivos e repetidores HDCP.

Essa consulta é equivalente à consulta \_ COPPQueryHDCPKeyData DXVA usada no COPP (Certified Output Protection Protocol).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[Solicitações de status do OPM](opm-status-requests.md)
</dt> </dl>

 

 




