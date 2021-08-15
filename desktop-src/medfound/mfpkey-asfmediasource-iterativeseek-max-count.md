---
description: Define o número máximo de i iterações de pesquisa que a fonte de mídia do ASF usará quando executar a busca iterativa.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183ed13143260f9d6d5de67ba38fcff27ebfd5a6afb01c75a07e92497d571cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874249"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>Propriedade MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count

Define o número máximo de i iterações de pesquisa que a fonte de mídia do ASF usará quando executar a busca iterativa.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a fonte de mídia do ASF. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

Essa propriedade se aplica somente quando a busca iterativa está habilitada. Para obter mais informações, [consulte MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

O intervalo válido dessa propriedade é \[ de 1 a 10, \] inclusive. Com um número maior, a busca iterativa tende a ser mais precisa, mas demora mais.

O valor padrão é 5.

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

 

 




