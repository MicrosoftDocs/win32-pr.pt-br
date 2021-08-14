---
description: Define a tolerância, em milissegundos, que é usada quando a fonte de mídia ASF executa a busca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cfc1ef656e1cff3da4bb33f19a3c2176729035f94a194a4ede21354f5dbc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874127"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>Tolerância A MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ na propriedade \_ \_ MiliSecond

Define a tolerância, em milissegundos, que é usada quando a fonte de mídia ASF executa a busca iterativa.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a fonte de mídia do ASF. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

Essa propriedade se aplica somente quando a busca iterativa está habilitada. Para obter mais informações, [consulte MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

O algoritmo de busca iterativa será interrompido se encontrar um pacote cuja distância do tempo de busca está dentro da tolerância especificada. O valor padrão é 8000 milissegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




