---
description: Especifica a duração de um fluxo de byte, em unidades de 100 nanossegundos.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION atributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ba32b394fa776b5b70a5a649292ffa205132645b15c24a57591483c734b238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826726"
---
# <a name="mf_bytestream_duration-attribute"></a>Atributo MF \_ BYTESTREAM \_ DURATION

Especifica a duração de um fluxo de byte, em unidades de 100 nanossegundos.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Trate como um **valor LONGLONG.**

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Se o objeto que cria o fluxo de byte puder determinar a duração, ele poderá definir esse atributo. (Por exemplo, em um fluxo de rede, a duração pode fazer parte da descrição da sessão.)

Para obter o valor do atributo, chame **QueryInterface** no fluxo de byte para obter um ponteiro para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Esse atributo é um valor assinado, embora seja armazenado como **um UINT64.**

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de fluxo de byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




