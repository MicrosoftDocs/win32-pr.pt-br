---
description: Define uma janela para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813986"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>\_Propriedade de janela MFPKEY http \_ bytes \_ Urlmon \_

Define uma janela para o Microsoft Media Foundation fluxo de bytes HTTP. A janela é usada para apresentar informações na interface do usuário durante uma operação de associação.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**IUnknown\***

VT \_ desconhecido

**punkVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

O valor dessa propriedade é um ponteiro para a interface **IWindowForBindingUI** . Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
