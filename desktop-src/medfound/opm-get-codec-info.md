---
description: Obtém o valor de mérito de um codec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847976"
---
# <a name="opm_get_codec_info"></a>\_informações do \_ codec de obtenção de OPM \_

Obtém o valor de mérito de um codec de hardware.



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------------|
| GUID de solicitação | **\_informações do \_ codec de obtenção de OPM \_**                                                                 |
| Dados de entrada   | Uma estrutura de [**parâmetros de informações de codec de \_ obtenção \_ \_ \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Retornar dados  | Uma estrutura de informação de informações do [**\_ codec de \_ \_ informações \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Comentários

Embora esse comando use a interface do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM), ele se aplica somente a codificadores de hardware e decodificadores. Ele não se aplica a dispositivos de saída de vídeo.

Em geral, você não deve usar esse comando diretamente. Para obter o valor de mérito para um codec de hardware, chame a função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Essa função executa todas as chamadas de OPM necessárias para enviar o comando **OPM \_ Get \_ codec \_ info** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Solicitações de status OPM](opm-status-requests.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




