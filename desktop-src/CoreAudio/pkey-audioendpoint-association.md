---
description: A \_ propriedade de associação PKEY AudioEndpoint \_ associa uma categoria de PIN de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756018"
---
# <a name="pkey_audioendpoint_association"></a>PKEY \_ AudioEndpoint \_ Association

A propriedade de **\_ \_ Associação PKEY AudioEndpoint** associa uma categoria de PIN de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio. O arquivo. inf que instala um adaptador de áudio atribui uma categoria de PIN a cada PIN KS no adaptador. Um PIN KS em um dispositivo de adaptador representa o ponto em que um fluxo de áudio entra ou sai do dispositivo. Uma categoria de PIN é um GUID que especifica o tipo de função executada por um PIN KS. Por exemplo, o arquivo de cabeçalho Ksmedia. h define o PIN da categoria de fixação KSNODETYPE \_ microfone para indicar um PIN KS que se conecta a um microfone e \_ fone de ouvido para indicar um PIN KS que se conecta aos fones de ouvido. Para obter mais informações, consulte a descrição das propriedades de categoria do PIN na documentação do Windows DDK.

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.

O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID de categoria de PIN KS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




