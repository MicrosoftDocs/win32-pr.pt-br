---
description: Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Atributo MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780073"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




