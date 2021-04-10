---
description: Lista de URLs para as quais a fonte de rede enviará informações de log.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Propriedade MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090687"
---
# <a name="mfnetsource_logurl-property"></a>\_Propriedade MFNETSOURCE LogURL

Lista de URLs para as quais a fonte de rede enviará informações de log.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Matriz de cadeias de caracteres largos (**CALPWSTR**)

\_LPWStr do vetor VT VT \| \_

**calpwstr**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ LogURL** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




