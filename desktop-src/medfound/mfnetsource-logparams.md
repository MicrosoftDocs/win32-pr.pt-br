---
description: Matriz de cadeias de caracteres com os parâmetros a enviar ao servidor de log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba557c4fb0bf77693669e8cb46af269ec3a4f2ed72c536e4bdab53a0778dc038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113516"
---
# <a name="mfnetsource_logparams-property"></a>Propriedade MFNETSOURCE \_ LOGPARAMS

Matriz de cadeias de caracteres com os parâmetros a enviar ao servidor de log.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A **constante \_ LOGPARAMS MFNETSOURCE** define o GUID para a chave de propriedade. O PID (identificador de propriedade) é zero. Para definir essa propriedade na origem da rede, passe **um ponteiro IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




