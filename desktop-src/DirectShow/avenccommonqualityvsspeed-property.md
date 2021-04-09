---
description: Especifica a compensação entre a qualidade de codificação e a velocidade. Essa propriedade é válida em todos os modos de controle de taxa.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propriedade AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087847"
---
# <a name="avenccommonqualityvsspeed-property"></a>Propriedade AVEncCommonQualityVsSpeed

Especifica a compensação entre a qualidade de codificação e a velocidade. Essa propriedade é válida em todos os modos de controle de taxa.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o seguinte intervalo.



| Valor | Descrição                      |
|-------|----------------------------------|
| 0     | Menor qualidade e codificação mais rápida.  |
| 100   | Maior qualidade, codificação mais lenta. |



 

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

 

 




