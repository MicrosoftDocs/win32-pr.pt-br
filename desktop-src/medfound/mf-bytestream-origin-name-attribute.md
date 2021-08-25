---
description: Especifica a URL original para um fluxo de bytes.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Atributo MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc485beeaf2b3fb80b7dc231dedf4082b848e003d0128c0cf4c73e8c2c5cc3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941056"
---
# <a name="mf_bytestream_origin_name-attribute"></a>\_Atributo de \_ nome de origem MF bytes \_

Especifica a URL original para um fluxo de bytes.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Os fluxos de bytes baseados em arquivo podem dar suporte a esse atributo. O valor do atributo é definido quando o fluxo de bytes é criado. Para obter o valor do atributo, consulte o objeto de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de fluxo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




