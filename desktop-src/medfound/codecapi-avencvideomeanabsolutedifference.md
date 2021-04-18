---
description: Controla a sinalização de MFSampleExtension \_ MeanAbsoluteDifference por meio de IMFAttribute em cada exemplo de saída.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Propriedade CODECAPI_AVEncVideoMeanAbsoluteDifference (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781192"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>\_Propriedade CODECAPI AVEncVideoMeanAbsoluteDifference

Controla a sinalização de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) por meio de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) em cada exemplo de saída.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>Comentários

Se o aplicativo definir um valor diferente de zero, o codificador deverá adicionar o atributo de exemplo [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a cada exemplo de saída. O \_ atributo MFSampleExtension MeanAbsoluteDifference indica a diferença absoluta média entre os exemplos de origem e os exemplos previstos no plano Y.

Se o codificador retornar 0 para **GetParameterRange**, o codificador não oferecerá suporte à saída de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) nos exemplos de saída.

O valor padrão deve ser 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




