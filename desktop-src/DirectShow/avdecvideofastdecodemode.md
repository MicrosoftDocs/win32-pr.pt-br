---
description: Obtém ou define a velocidade de decodificação de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propriedade AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087854"
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
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




