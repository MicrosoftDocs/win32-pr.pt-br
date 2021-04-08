---
description: Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010661"
---
# <a name="opm_get_dvi_characteristics"></a>OPM \_ obter \_ características de DVI \_

Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitação | OPM \_ obter \_ características de DVI \_                                              |
| Dados de entrada   | Nenhum                                                                        |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentários

Se essa consulta for realizada com sucesso, o membro **ulInformation** da estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contém um dos valores a seguir.



| Valor                                     | Descrição               |
|-------------------------------------------|---------------------------|
| Característica de DVI de OPM \_ \_ \_ 1 \_ 0            | DVI versão 1,0.          |
| \_Característica DVI de OPM \_ \_ 1 \_ 1 \_ ou \_ acima | DVI versão 1,1 ou posterior. |



 

Essa consulta só tem suporte quando o tipo de conector físico é um tipo de conector de OPM \_ \_ \_ DVI. Para obter o tipo de conector, envie a consulta de [**\_ \_ \_ tipo de conector do OPM**](opm-get-connector-type.md) .

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

 

 




