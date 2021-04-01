---
description: Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164899"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ definido \_ SRM de HDCP \_

Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ definido \_ SRM de HDCP \_                                                                 |
| Dados de entrada   | Uma estrutura de [**\_ parâmetros de \_ \_ SRM \_ de HDCP definido de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

O parâmetro *pbAdditionalParameters* de [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) deve apontar para um buffer que contém o SRM. O formato de um SRM de HDCP é documentado na especificação de HDCP. Defina o parâmetro *ulAdditionalParametersSize* igual ao tamanho do buffer, em bytes.

## <a name="remarks"></a>Comentários

SRMs são usados para atualizar a lista de dispositivos HDCP revogados. SRMs são entregues com o conteúdo de vídeo.

Esse comando atualiza o SRM atual da saída de vídeo. Se a HDCP estiver habilitada no momento do comando, a saída de vídeo usará o novo SRM para verificar se algum dos dispositivos de HDCP conectados está revogado. Se a saída de vídeo detectar um dispositivo revogado, ele interromperá a exibição do vídeo. Se você enviar esse comando enquanto o HDCP estiver desabilitado, a saída de vídeo validará o SRM e o armazenará. Posteriormente, se o aplicativo habilitar a HDCP, a saída de vídeo usará o novo SRM para verificar o status de revogação do dispositivo.

Esse comando pode fazer com que o método **Configure** retorne qualquer um dos códigos de erro a seguir.



| Código de retorno                                            | Descrição                             |
|--------------------------------------------------------|-----------------------------------------|
| gráficos de erro \_ \_ OPM \_ \_ SRM inválido                     | O SRM não é válido.                   |
| ERRO \_ gráficos \_ de \_ saída \_ OPM \_ não \_ dá suporte a \_ HDCP | A saída de vídeo não oferece suporte a HDCP. |



 

Não há suporte para esse comando quando a interface **IOPMVideoOutput** emula o protocolo Copp (certificado de proteção de saída). Quando semântica COPP é usada, o aplicativo é responsável por analisar SRMs e verificar o status de revogação do dispositivo HDCP. Use a solicitação de status de [informações do dispositivo OPM- \_ \_ conectado \_ HDCP \_ \_ ](opm-get-connected-hdcp-device-information.md) para obter o vetor de seleção de chave (KSV) do dispositivo, que é necessário para verificar o status de revogação. Para obter mais informações sobre SRMs, consulte a especificação de HDCP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




