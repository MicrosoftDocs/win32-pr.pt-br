---
description: A propriedade PKEY \_ AudioEndpoint JackSubType contém um GUID de categoria de \_ saída para um dispositivo de ponto de extremidade de áudio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053726"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

A **propriedade PKEY \_ AudioEndpoint \_ JackSubType** contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio. O arquivo de header Ksmedia.h define os GUIDs; cada GUID especifica o tipo de conexão. Esses GUIDs também têm categorias de pino associadas. Por exemplo, o arquivo de header Ksmedia.h define a INTERFACE GUID **KSNODETYPE \_ \_ DISPLAYPORT** para uma porta de exibição que se conecta ao pino KS definido pelo GUID **PINNAME \_ DISPLAYPORT \_ OUT.**

Para obter mais informações, consulte a descrição das propriedades de fixar categoria na documentação Windows DDK.

O **membro vt** da estrutura **PROPVARIANT** é definido como **VT \_ LPWSTR.**

O **membro pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID de categoria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio principais](core-audio-properties.md)
</dt> </dl>

 

 




