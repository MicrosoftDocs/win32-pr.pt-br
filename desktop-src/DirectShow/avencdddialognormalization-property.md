---
description: Especifica o nível de normalização da caixa de diálogo, em dB (decib), em um fluxo de áudio Dolby Digital. Essa propriedade se aplica a codificadores de áudio Dolby Digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propriedade AVEncDDDialogNormalization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f050147b0de889c9bb12f4e66964f16b8705c4883fa66c0f5cbba9c82338c30f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690186"
---
# <a name="avencdddialognormalization-property"></a>Propriedade AVEncDDDialogNormalization

Especifica o nível de normalização da caixa de diálogo, em dB (decib), em um fluxo de áudio Dolby Digital. Essa propriedade se aplica a codificadores de áudio Dolby Digital.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncDDDialogNormalization**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




