---
description: Especifica a taxa de bits mínima, em bits por segundo. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Propriedade AVEncCommonMinBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65488b3a855d4b664c96a1d7abfc1718a35e94c466877c68848a1acf25a3bfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159852"
---
# <a name="avenccommonminbitrate-property"></a>Propriedade AVEncCommonMinBitRate

Especifica a taxa de bits mínima, em bits por segundo. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMinBitRate**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentários

O codificador impõe a taxa de bits mínima aumentando a qualidade da codificação conforme necessário.

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

 

 




