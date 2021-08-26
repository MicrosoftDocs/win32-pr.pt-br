---
description: Habilita ou desabilita a equalização de intensidade em um decodificador de áudio ou em um processador de sinais digitais (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propriedade AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61696b51996d6fe57cf15372d511704e2dad482f0a5e99eb165795f56256656a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052826"
---
# <a name="avdsploudnessequalization-property"></a>Propriedade AVDSPLoudnessEqualization

Habilita ou desabilita a equalização de intensidade em um decodificador de áudio ou em um processador de sinais digitais (DSP).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .

## <a name="remarks"></a>Comentários

A equalização de intensidade é um processo de DSP que mantém um nível de volume consistente quando o fluxo de áudio é alterado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




