---
description: Define o nível de proteção para um mecanismo de proteção de saída.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791357"
---
# <a name="opm_set_protection_level"></a>OPM \_ definir \_ nível de proteção \_

Define o nível de proteção para um mecanismo de proteção de saída.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ definir \_ nível de proteção \_                                                                         |
| Dados de entrada   | Uma estrutura de [**parâmetros de nível de proteção dos OPMS \_ definidos \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Comentários

Alguns conectores podem dar suporte a vários mecanismos de proteção. Com esse tipo de conector, você pode aplicar vários mecanismos de proteção ao mesmo conector, com configurações diferentes para cada um.

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

 

 




