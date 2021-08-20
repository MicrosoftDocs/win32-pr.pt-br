---
description: Define os sinalizadores de associação de moniker para o fluxo de Microsoft Media Foundation de byte HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbc2c32491caa327b1f7a54d4c9738dddf9dde3ad08efcd4eb075cd37995d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690131"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>Propriedade Sinalizadores de Vinculação de Urlmon de Urlmon de \_ Http \_ ByteStream \_ \_ \_ MFPKEY

Define os sinalizadores de associação de moniker para o fluxo de Microsoft Media Foundation de byte HTTP.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o fluxo de Media Foundation de byte HTTP. Para definir a propriedade , passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

O valor dessa propriedade é um **OR** bit a bit de sinalizadores da **enumeração BINDF.** Essa propriedade se aplica somente quando a [propriedade \_ MFPKEY HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) é definida como **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
