---
description: 'Saiba mais sobre: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502266"
---
# <a name="opm_get_connected_hdcp_device_information"></a>\_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_

Obtém informações sobre um dispositivo de Proteção de Conteúdo High-Bandwidth digital (HDCP) anexado à saída de vídeo. As seguintes informações são retornadas:

-   O vetor de seleção de chave de HDCP do dispositivo (KSV).
-   Se o dispositivo é um repetidor HDCP.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID de solicitação | \_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_                                                          |
| Dados de entrada   | Nenhum                                                                                                    |
| Retornar dados  | Uma estrutura de [**\_ informações de \_ \_ dispositivo \_ de HDCP conectada por OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Comentários

Essa consulta pode ser usada somente com o *modo de emulação Copp*. Se a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usar a semântica de OPM (Gerenciador de proteção de saída), essa solicitação de status não terá suporte.

O KSV é um identificador fornecido para o fabricante do dispositivo e é usado no processo de autenticação e configuração de HDCP. No modo de emulação COPP, o aplicativo usa o KSV para determinar se o dispositivo HDCP foi revogado. Se for, o aplicativo não deverá reproduzir o conteúdo protegido. Além disso, o aplicativo não deve reproduzir conteúdo protegido se o dispositivo for um repetidor HDCP, porque a COPP não dá suporte a repetidores de HDCP.

Essa consulta não é necessária quando é usada semântica de OPM, pois o OPM dá suporte à revogação de dispositivo e repetidores de HDCP.

Essa consulta é equivalente à consulta DXVA \_ COPPQueryHDCPKeyData usada no protocolo de proteção de saída certificado (Copp).

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

[Solicitações de status OPM](opm-status-requests.md)
</dt> </dl>

 

 




