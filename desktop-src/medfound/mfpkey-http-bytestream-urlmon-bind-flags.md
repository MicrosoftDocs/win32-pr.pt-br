---
description: Define os sinalizadores de associação do moniker para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781112"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>\_Propriedade de sinalizadores de associação MFPKEY http \_ bytes \_ Urlmon \_ \_

Define os sinalizadores de associação do moniker para o Microsoft Media Foundation fluxo de bytes HTTP.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

O valor dessa propriedade é um bit a bit **ou** dos sinalizadores da enumeração **BINDF** . Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
