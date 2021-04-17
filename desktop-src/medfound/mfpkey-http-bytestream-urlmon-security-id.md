---
description: Define o identificador de segurança raiz para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759803"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>\_Propriedade de ID de segurança MFPKEY http \_ bytes \_ Urlmon \_ \_

Define o identificador de segurança raiz para o Microsoft Media Foundation fluxo de bytes HTTP.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**CAUB**

\_UI1 de vetor \| VT \_ VT

**caub**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
