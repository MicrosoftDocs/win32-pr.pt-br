---
description: O valor do campo &\# 0034; c-hostexe&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Propriedade MFNETSOURCE_HOSTEXE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663013"
---
# <a name="mfnetsource_hostexe-property"></a>\_Propriedade MFNETSOURCE HOSTEXE

O valor do campo "c-hostexe" usado pela fonte de rede para registro em log. Os aplicativos podem definir essa propriedade como o nome do aplicativo host. Por exemplo, o valor pode ser "iexplore.exe" se o aplicativo estiver hospedado em uma página da Web.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ HOSTEXE** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Log de cliente](client-logging.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




