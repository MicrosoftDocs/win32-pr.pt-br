---
description: Especifica a taxa média de bits do fluxo de áudio codificado, em bits por segundo. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Propriedade AVEncAudioMeanBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7b0d1ad6cfde3aee4ec9c747feb8d692c3917332808e40e3d5f76e3d01ce21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079466"
---
# <a name="avencaudiomeanbitrate-property"></a>Propriedade AVEncAudioMeanBitRate

Especifica a taxa média de bits do fluxo de áudio codificado, em bits por segundo. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valor da propriedade

Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional aplicativos \[ UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




