---
description: Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787713"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_

Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitação | OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_                                       |
| Dados de entrada   | Nenhum                                                                        |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentários

Se essa consulta for realizada com sucesso, o membro **ulInformation** da estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contém o número de versão do SRM, no formato little-endian.

SRMs são usados para atualizar a lista de dispositivos de High-Bandwidth digital Proteção de Conteúdo (HDCP) revogados. SRMs são entregues com o conteúdo de vídeo. Para definir o SRM, envie o comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Essa consulta pode fazer com que o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorne qualquer um dos códigos de erro a seguir.



| Código de retorno                                            | Descrição                             |
|--------------------------------------------------------|-----------------------------------------|
| gráfico de erros \_ \_ OPM de HDCP do \_ \_ SRM \_ nunca \_ definido            | O aplicativo não definiu um SRM.     |
| ERRO \_ gráficos \_ de \_ saída \_ OPM \_ não \_ dá suporte a \_ HDCP | A saída de vídeo não oferece suporte a HDCP. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitações de status OPM](opm-status-requests.md)
</dt> </dl>

 

 




