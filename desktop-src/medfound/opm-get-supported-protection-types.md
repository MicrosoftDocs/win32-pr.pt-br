---
description: Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012536"
---
# <a name="opm_get_supported_protection_types"></a>os \_ tipos de proteção de OPM \_ têm suporte \_ \_

Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitação | os \_ tipos de proteção de OPM \_ têm suporte \_ \_                                      |
| Dados de entrada   | Nenhum                                                                        |
| Retornar dados  | Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentários

Os mecanismos de proteção são retornados no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O valor é um dos sinalizadores de [tipo de proteção](opm-protection-type-flags.md)de bits **ou** de Unificação de OPM.

Essa consulta é equivalente à consulta DXVA \_ COPPQueryProtectionType usada no protocolo de proteção de saída certificado (Copp).

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

 

 




