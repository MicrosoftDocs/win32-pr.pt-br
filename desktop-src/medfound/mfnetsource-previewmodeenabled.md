---
description: Habilita ou desabilita o modo de visualização, o que permite que o aplicativo substitua a lógica de buffer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Propriedade MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749957"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>\_Propriedade MFNETSOURCE PREVIEWMODEENABLED

Habilita ou desabilita o modo de visualização, o que permite que o aplicativo substitua a lógica de buffer inicial.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL**

BOOL do VT \_

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define o GUID da chave de propriedade. O identificador de propriedade (PID) é zero. Essa propriedade é definida na fonte de rede passando um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

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

 

 




