---
description: Armazena a cadeia de caracteres enviada no cabeçalho de Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Propriedade MFNETSOURCE_STREAM_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370518"
---
# <a name="mfnetsource_stream_language-property"></a>Propriedade de linguagem de \_ fluxo MFNETSOURCE \_

Armazena a cadeia de caracteres enviada no cabeçalho de Accept-Language.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**WCHAR \** _

LPWStr do VT \_

_ *pwszVal**



## <a name="remarks"></a>Comentários

A \_ constante de linguagem de fluxo MFNETSOURCE \_ define o GUID da chave de propriedade. O identificador de propriedade (PID) é zero. Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




