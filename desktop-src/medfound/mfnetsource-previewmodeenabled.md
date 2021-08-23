---
description: Habilita ou desabilita o modo de visualização, que permite que o aplicativo sobrescreva a lógica de buffer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03940828c6fa32b9e0367a03f960d4d64d88edf691100817ed31883013ce1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663856"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>Propriedade MFNETSOURCE \_ PREVIEWMODEENABLED

Habilita ou desabilita o modo de visualização, que permite que o aplicativo sobrescreva a lógica de buffer inicial.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Bool**

BOOL da VT \_

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define o GUID para a chave de propriedade. O PID (identificador de propriedade) é zero. Essa propriedade é definida na origem da rede passando um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

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

 

 




