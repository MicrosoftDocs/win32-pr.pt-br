---
description: Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propriedade AVDecAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825935"
---
# <a name="avdecaudiodualmono-property"></a>Propriedade AVDecAudioDualMono

Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .

## <a name="remarks"></a>Comentários

Essa propriedade só se aplica quando o fluxo de bits de entrada do decodificador contém áudio de dois canais. Um fluxo de áudio de dois canais pode ser codificado como estéreo ou mono duplo. Se o áudio for dual mono, você poderá definir a propriedade [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar como o decodificador reproduzirá o áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




