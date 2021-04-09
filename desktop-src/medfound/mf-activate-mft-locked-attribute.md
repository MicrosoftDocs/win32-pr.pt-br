---
description: Especifica se o carregador de topologia alterará os tipos de mídia em uma Media Foundation transformação (MFT). Normalmente, os aplicativos não usam esse atributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Atributo MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091159"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ Ativar \_ atributo do MFT \_ bloqueado

Especifica se o carregador de topologia alterará os tipos de mídia em uma Media Foundation transformação (MFT). Normalmente, os aplicativos não usam esse atributo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se o valor desse atributo for diferente de zero, o carregador de topologia não alterará os tipos de mídia no MFT. O carregador de topologia define esse atributo depois de carregar a topologia.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




