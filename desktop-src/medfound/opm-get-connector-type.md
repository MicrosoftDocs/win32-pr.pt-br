---
description: Retorna o tipo de conector físico da saída de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099da66193048b52011e58eb5ce3f925d451fc1ad26b193f2955f6012f0e607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887496"
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

 

 




