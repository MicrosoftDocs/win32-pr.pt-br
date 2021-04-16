---
title: EQUALIZERSETTINGS. normalização
description: O atributo de normalização especifica ou recupera um valor que indica se a normalização está habilitada.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalização do Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779422"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS. normalização

O atributo de **normalização** especifica ou recupera um valor que indica se a normalização está habilitada.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                         |
|-------|-------------------------------------|
| true  | A normalização está habilitada.           |
| false | Padrão. A normalização está desabilitada. |



 

## <a name="remarks"></a>Comentários

Quando a normalização é habilitada, o sinal de áudio de um arquivo de mídia digital inteiro é dimensionado para o valor máximo. Isso permite que vários arquivos sejam reproduzidos em aproximadamente o mesmo volume sem a necessidade de ajustes de volume.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





