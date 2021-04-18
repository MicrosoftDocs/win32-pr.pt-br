---
description: Habilita o modo de download particular na fonte de rede.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Propriedade MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790384"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ habilitar \_ Propriedade particularmode

Habilita o modo de download particular na fonte de rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL**

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

Se essa propriedade for **true**, o cache será limpo quando a sessão terminar.

A constante **MFNETSOURCE \_ CLIENTGUID** define o GUID da chave de propriedade. O identificador de propriedade (PID) é zero. Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




