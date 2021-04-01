---
description: Especifica a taxa de bits máxima, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Propriedade AVEncCommonMaxBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825957"
---
# <a name="avenccommonmaxbitrate-property"></a>Propriedade AVEncCommonMaxBitRate

Especifica a taxa de bits máxima, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMaxBitRate**

## <a name="property-value"></a>Valor da propriedade

Esta propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




