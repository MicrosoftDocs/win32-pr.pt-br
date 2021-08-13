---
description: O valor do campo &\# 0034;c-hostexe&0034; que a fonte de rede usa para registro \# em log.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dbde4b4b445e88a0cb6e7ebe45b8b88f386c208854057f209d9c36b7e0024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463646"
---
# <a name="mfnetsource_hostexe-property"></a>Propriedade HOSTEXE MFNETSOURCE \_

O valor do campo "c-hostexe" que a fonte de rede usa para registro em log. Os aplicativos podem definir essa propriedade como o nome do aplicativo host. Por exemplo, o valor poderá ser "iexplore.exe" se o aplicativo estiver hospedado em uma página da Web.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **\_ HOSTEXE de MFNETSOURCE** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Registro em log do cliente](client-logging.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




