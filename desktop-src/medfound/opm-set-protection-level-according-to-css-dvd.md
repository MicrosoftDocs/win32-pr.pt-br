---
description: Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2290f8d0dd17e01d482c197a54448a3317b11f80840579c2ddd05f01b6103840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101895"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS

Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS                                                |
| Dados de entrada   | Uma estrutura de [**parâmetros de nível de proteção dos OPMS \_ definidos \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Comentários

Esse comando é usado para definir High-Bandwidth Proteção de Conteúdo Digital (HDCP) ao reproduzir DVDs padrão. Ao contrário do comando de [**\_ nível de \_ proteção \_ do OPM definido**](opm-set-protection-level.md) , se HDCP não puder ser definido por algum motivo, esse comando não interromperá a reprodução. (As regras de DVD CSS contêm um provisionamento de "melhor esforço" para os jogadores.) Caso contrário, esse comando é idêntico ao comando de **nível de proteção de OPM \_ set \_ Protection \_** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




