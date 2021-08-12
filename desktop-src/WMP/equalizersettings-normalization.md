---
title: EQUALIZERSETTINGS.normalization
description: O atributo de normalização especifica ou recupera um valor que indica se a normalização está habilitada.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS.normalization Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578159"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS.normalization

O **atributo de normalização** especifica ou recupera um valor que indica se a normalização está habilitada.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                         |
|-------|-------------------------------------|
| true  | A normalização está habilitada.           |
| false | Padrão. A normalização está desabilitada. |



 

## <a name="remarks"></a>Comentários

Quando a normalização está habilitada, o sinal de áudio para um arquivo de mídia digital inteiro é dimensionado para o valor máximo. Isso permite que vários arquivos sejam interpretados aproximadamente no mesmo volume sem a necessidade de ajustes de volume.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





