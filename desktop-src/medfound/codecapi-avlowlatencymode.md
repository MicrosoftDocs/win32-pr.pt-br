---
description: Habilita o modo de baixa latência em um codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1466f7874fe743dbc865df251f077440885103853e3784af19624c4733a1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606266"
---
# <a name="codecapi_avlowlatencymode-property"></a>Propriedade CODECAPI \_ AVLowLatencyMode

Habilita o modo de baixa latência em um codec.

## <a name="data-type"></a>Tipo de dados

**ULONG** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valor da propriedade

Se o valor for diferentes de zero, o modo de baixa latência será habilitado. Se o valor for zero, o modo de baixa latência será desabilitado.

## <a name="remarks"></a>Comentários

Essa propriedade se aplica a codificadores e decodificadores.

O modo de baixa latência é útil para comunicações em tempo real ou captura ao vivo, quando a latência deve ser minimizada. No entanto, o modo de baixa latência também pode reduzir a qualidade de decodificação ou codificação.

Espera-se que o codificador não adicione nenhum atraso de exemplo devido à reordenação de quadros no processo de codificação e uma amostra de entrada deverá produzir uma amostra de saída. Fatias/quadros B podem estar presentes, desde que não introduzam nenhuma nova ordenação de quadro no codificador.

> [!WARNING] 
> Na implementação atual, o decodificador Media Foundation H.264 usa o tipo **VT_UI4** para essa propriedade. Todas as outras implementações, incluindo o codificador H.264, usam o tipo **VT_BOOL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

