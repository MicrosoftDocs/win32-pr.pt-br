---
description: Define o identificador de segurança raiz para o fluxo Microsoft Media Foundation de byte HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64b07dc7d419624bfe300b890b58554394a5cd3e8363ddcbc4d5be91d9e4b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738003"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>Propriedade ID de segurança de Urlmon de Urlmon de \_ Http \_ ByteStream \_ \_ \_ MFPKEY

Define o identificador de segurança raiz para o fluxo Microsoft Media Foundation de byte HTTP.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**CAUB**

VT \_ VECTOR \| VT \_ UI1

**caub**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o fluxo de Media Foundation de byte HTTP. Para definir a propriedade , passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

Essa propriedade se aplica somente quando a [propriedade \_ MFPKEY HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) é definida como **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
