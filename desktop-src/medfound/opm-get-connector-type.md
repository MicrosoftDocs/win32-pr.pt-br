---
description: Retorna o tipo de conector físico da saída de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164904"
---
# <a name="opm_get_connector_type"></a>\_tipo de \_ conector de obtenção de OPM \_

Retorna o tipo de conector físico da saída de vídeo.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitação | \_tipo de \_ conector de obtenção de OPM \_                                                   |
| Dados de entrada   | Nenhum                                                                        |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentários

O tipo de conector é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O valor de **ulInformation** é igual a um dos tipos de conector listados nos [**sinalizadores de tipo de conector OPM**](opm-connector-type-flags.md).

No modo de emulação COPP, o tipo de conector pode ser combinado com o sinalizador **interno do tipo de \_ conector OPM Copp \_ compatível \_ \_ \_** . Use um **e bit e** para extrair o tipo de conector:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Os aplicativos devem ignorar o sinalizador **\_ \_ \_ \_ \_ interno do tipo conector compatível com OPM Copp** . Para obter mais informações, consulte a seção comentários dos [**sinalizadores de tipo de conector OPM**](opm-connector-type-flags.md).

Essa consulta é equivalente à consulta DXVA \_ COPPQueryConnectorType usada no protocolo de proteção de saída certificado (Copp).

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

 

 




