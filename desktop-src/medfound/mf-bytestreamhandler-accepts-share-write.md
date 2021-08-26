---
description: Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Atributo MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941026"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ aceita \_ o \_ atributo de gravação de compartilhamento

Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Os manipuladores de fluxo de bytes podem dar suporte a esse atributo. Para obter ou definir o atributo, primeiro consulte o manipulador de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Em seguida, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) ou [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Se esse atributo for **true**, significa que o manipulador de fluxo de bytes pode ler de um fluxo enquanto outro thread grava no mesmo fluxo. Quando um fluxo é aberto para gravação por outro thread, o método [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) retorna o sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** .

Esse atributo afeta a resolução da origem. Se um fluxo de bytes tiver o sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** definido, o [resolvedor de origem](source-resolver.md) não passará esse fluxo para um manipulador de fluxo de bytes, a menos que o manipulador tenha o suplemento MF \_ BYTESTREAMHANDLER aceite o \_ \_ \_ atributo de gravação de compartilhamento definido como **true**.

O sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** é uma dica que o comprimento do fluxo pode mudar enquanto o manipulador está lendo nele.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




