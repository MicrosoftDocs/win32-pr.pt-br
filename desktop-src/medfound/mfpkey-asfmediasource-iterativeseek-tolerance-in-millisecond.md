---
description: Define a tolerância, em milissegundos, que é usada quando a origem de mídia do ASF executa a busca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810760"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerância \_ na \_ propriedade de milissegundos

Define a tolerância, em milissegundos, que é usada quando a origem de mídia do ASF executa a busca iterativa.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a origem da mídia ASF. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Essa propriedade só se aplica quando a busca iterativa está habilitada. Para obter mais informações, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

O algoritmo de busca interativa é interrompido se encontrar um pacote cuja distância do tempo de busca está dentro da tolerância especificada. O valor padrão é 8000 milissegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




