---
description: Matriz de cadeias de caracteres com os parâmetros a serem enviados ao servidor de log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Propriedade MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921265"
---
# <a name="mfnetsource_logparams-property"></a>\_Propriedade MFNETSOURCE LOGPARAMS

Matriz de cadeias de caracteres com os parâmetros a serem enviados ao servidor de log.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**WCHAR \** _

LPWStr do VT \_

_ *pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ LOGPARAMS** define o GUID da chave de propriedade. O identificador de propriedade (PID) é zero. Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

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

 

 




