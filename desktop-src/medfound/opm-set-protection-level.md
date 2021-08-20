---
description: Define o nível de proteção para um mecanismo de proteção de saída.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83203f68d0a55af3be2d407aab9831576544910e37f938b6539cb16d40d9b26b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058703"
---
# <a name="opm_set_protection_level"></a>OPM \_ SET \_ PROTECTION \_ LEVEL

Define o nível de proteção para um mecanismo de proteção de saída.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ SET \_ PROTECTION \_ LEVEL                                                                         |
| Dados de entrada   | Uma [**estrutura OPM \_ SET PROTECTION \_ LEVEL \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Comentários

Alguns conectores podem dar suporte a vários mecanismos de proteção. Com esse tipo de conector, você pode aplicar vários mecanismos de proteção ao mesmo conector, com configurações diferentes para cada um.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos do OPM](opm-commands.md)
</dt> </dl>

 

 




