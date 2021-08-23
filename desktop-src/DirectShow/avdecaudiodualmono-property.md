---
description: Propriedade AVDecAudioDualMono – especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propriedade AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a26bd6685cb9c9f326babbc01120019c93760fd7e1f9bf33f2a540d488300ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873386"
---
# <a name="avdecaudiodualmono-property"></a>Propriedade AVDecAudioDualMono

Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDecAudioDualMono.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)

## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente quando o fluxo de bits de entrada do decodificador contém áudio de dois canais. Um fluxo de áudio de dois canais pode ser codificado como estéreo ou como mono duplo. Se o áudio for mono duplo, você poderá definir a propriedade [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar como o decodificador reproduz o áudio.

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

 

 




