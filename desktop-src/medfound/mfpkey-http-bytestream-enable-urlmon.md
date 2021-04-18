---
description: Habilita o Microsoft Media Foundation fluxo de bytes HTTP para usar identificadores de URL (também chamados de Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Propriedade MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778455"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ http \_ bytes \_ habilitar a \_ Propriedade Urlmon

Habilita o Microsoft Media Foundation fluxo de bytes HTTP para usar identificadores de URL (também chamados de *Urlmon*).



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Se o valor for **Variant \_ true**, o fluxo de bytes http usará Urlmon para transporte http. Caso contrário, se o valor for **Variant \_ false**, o fluxo de bytes usará o WinHTTP.

O valor padrão é **Variant \_ true** para aplicativos da Windows Store e **variante \_ false** para o aplicativo da área de trabalho do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
