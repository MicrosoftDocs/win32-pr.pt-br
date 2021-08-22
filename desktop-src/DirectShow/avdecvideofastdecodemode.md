---
description: Obtém ou define a velocidade de decodificação de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propriedade AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36cd765754e73924caae401495e597ec69828ed62f08466884b10365517d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503134"
---
# <a name="avdecvideofastdecodemode-property"></a>Propriedade AVDecVideoFastDecodeMode

Obtém ou define a velocidade de decodificação de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade pode variar de 0 a 32, onde 0 indica que a decodificação normal e 32 é o modo de decodificação mais rápida. O comportamento exato depende da implementação do decodificador. Nem todo incremento entre 1 e 32 define necessariamente é um modo distinto.

A enumeração [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contém alguns modos predefinidos para essa propriedade.

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

 

 




