---
description: Especifica se o Carregador de Topologia alterará os tipos de mídia em uma transformação Media Foundation (MFT). Normalmente, os aplicativos não usam esse atributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060906"
---
# <a name="mf_activate_mft_locked-attribute"></a>Atributo MF \_ ACTIVATE \_ MFT \_ LOCKED

Especifica se o Carregador de Topologia alterará os tipos de mídia em uma transformação Media Foundation (MFT). Normalmente, os aplicativos não usam esse atributo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Se o valor desse atributo for diferentes de zero, o carregador de topologia não alterará os tipos de mídia no MFT. O carregador de topologia define esse atributo depois de carregar a topologia.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




