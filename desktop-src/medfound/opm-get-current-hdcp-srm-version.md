---
description: Retorna o número de versão da SRM (mensagem de renovação do sistema) usada atualmente pela saída de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee36516510d04fec067bbc692387e2e36b9da083db1a6daae0f51948a992cc83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887486"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OBTER \_ A \_ VERSÃO ATUAL DO \_ \_ HDCP SRM \_ DO OPM

Retorna o número de versão da SRM (mensagem de renovação do sistema) usada atualmente pela saída de vídeo.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitação | OBTER \_ A \_ VERSÃO ATUAL DO \_ \_ HDCP SRM \_ DO OPM                                       |
| Dados de entrada   | Nenhum                                                                        |
| Retornar dados  | Uma [**estrutura de INFORMAÇÕES PADRÃO \_ \_ do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentários

Se essa consulta for bem-sucedida, o membro **ulInformation** da estrutura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) conterá o número de versão srm, no formato little-endian.

OS SRMs são usados para atualizar a lista de dispositivos High-Bandwidth HDCP (Proteção de Conteúdo Digital). OS SRMs são entregues com o conteúdo do vídeo. Para definir o SRM, envie o comando [**OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Essa consulta pode fazer com que [**o método IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorne qualquer um dos códigos de erro a seguir.



| Código de retorno                                            | Descrição                             |
|--------------------------------------------------------|-----------------------------------------|
| GRÁFICOS \_ DE \_ ERRO OPM \_ HDCP \_ SRM NUNCA \_ \_ DEFINIDO            | O aplicativo não definiu um SRM.     |
| GRÁFICOS \_ DE ERRO A SAÍDA DO \_ OPM NÃO DÁ \_ SUPORTE AO \_ \_ \_ \_ HDCP | A saída de vídeo não dá suporte ao HDCP. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitações de status do OPM](opm-status-requests.md)
</dt> </dl>

 

 




