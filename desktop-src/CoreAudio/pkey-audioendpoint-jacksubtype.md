---
description: A \_ Propriedade PKEY AudioEndpoint \_ JackSubType contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089515"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

A propriedade **PKEY \_ AudioEndpoint \_ JACKSUBTYPE** contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio. O arquivo de cabeçalho Ksmedia. h define os GUIDs; cada GUID especifica o tipo de conexão. Esses GUIDs também têm categorias de PIN associadas. Por exemplo, o arquivo de cabeçalho Ksmedia. h define **a \_ \_ interface do GUID KSNODETYPE DisplayPort** para uma porta de exibição que se conecta com o PIN KS definido pelo GUID **PINNAME \_ DisplayPort \_ out**.

Para obter mais informações, consulte a descrição das propriedades de categoria do PIN na documentação do Windows DDK.

O membro **VT** da estrutura **PROPVARIANT** é definido como **VT \_ LPWSTR**.

O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID de categoria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




