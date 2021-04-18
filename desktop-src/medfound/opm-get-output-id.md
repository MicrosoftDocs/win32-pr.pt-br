---
description: Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796168"
---
# <a name="opm_get_output_id"></a>\_ID de \_ saída de obtenção de OPM \_

Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.



| Requisito | Valor |
|--------------|------------------------------------------------------------------|
| GUID de solicitação | \_ID de \_ saída de obtenção de OPM \_                                             |
| Dados de entrada   | Nenhum                                                             |
| Retornar dados  | Uma estrutura de [**\_ dados de \_ ID \_ de saída OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) |



 

## <a name="remarks"></a>Comentários

O driver de vídeo atribui um identificador exclusivo a cada monitor. Essa consulta retorna o identificador do monitor que está associado ao ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) atual.

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

 

 




