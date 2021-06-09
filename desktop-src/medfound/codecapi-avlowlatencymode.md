---
description: Habilita o modo de baixa latência em um codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Propriedade CODECAPI_AVLowLatencyMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826900"
---
# <a name="codecapi_avlowlatencymode-property"></a>\_Propriedade CODECAPI AVLowLatencyMode

Habilita o modo de baixa latência em um codec.

## <a name="data-type"></a>Tipo de dados

**ULONG** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valor da propriedade

Se o valor for diferente de zero, o modo de baixa latência será habilitado. Se o valor for zero, o modo de baixa latência será desabilitado.

## <a name="remarks"></a>Comentários

Essa propriedade se aplica a codificadores e decodificadores.

O modo de baixa latência é útil para comunicações em tempo real ou captura dinâmica, quando a latência deve ser minimizada. No entanto, o modo de baixa latência também pode reduzir a codificação ou a qualidade da codificação.

Espera-se que o codificador não adicione nenhum atraso de exemplo devido à reordenação do quadro no processo de codificação, e um exemplo de entrada deve produzir um exemplo de saída. B fatias/quadros podem estar presentes desde que não introduzam nenhuma reordenação de quadro no codificador.

> [!WARNING] 
> Na implementação atual, o decodificador Media Foundation H. 264 usa o tipo **VT_UI4** para essa propriedade. Todas as outras implementações, incluindo o codificador H. 264, usam o tipo **VT_BOOL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

